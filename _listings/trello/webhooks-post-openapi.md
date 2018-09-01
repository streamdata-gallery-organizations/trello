---
swagger: "2.0"
x-collection-name: Trello
x-complete: 0
info:
  title: Trello Post Webhooks
  description: Post webhooks.
  termsOfService: https://trello.com/legal
  contact:
    name: Trello
    url: https://trello.com/home
  version: "1.0"
host: trello.com
basePath: /1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /actions/{idAction}:
    delete:
      summary: Delete Actions
      description: Delete actions.
      operationId: deleteActionsByIdAction
      x-api-path-slug: actionsidaction-delete
      parameters:
      - in: path
        name: idAction
        description: idAction
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Actions
    get:
      summary: Get Actions
      description: Get actions.
      operationId: getActionsByIdAction
      x-api-path-slug: actionsidaction-get
      parameters:
      - in: query
        name: display
        description: true or false
      - in: query
        name: entities
        description: true or false
      - in: query
        name: fields
        description: 'all or a comma-separated list of: data, date, idMemberCreator
          or type'
      - in: path
        name: idAction
        description: idAction
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: member
        description: true or false
      - in: query
        name: memberCreator
        description: true or false
      - in: query
        name: memberCreator_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Actions
    put:
      summary: Put Actions
      description: Put actions.
      operationId: updateActionsByIdAction
      x-api-path-slug: actionsidaction-put
      parameters:
      - in: body
        name: body
        description: Attributes of Actions to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idAction
        description: idAction
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Actions
  /actions/{idAction}/board:
    get:
      summary: Get Actions Board
      description: Get actions board.
      operationId: getActionsBoardByIdAction
      x-api-path-slug: actionsidactionboard-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: closed, dateLastActivity,
          dateLastView, desc, descData, idOrganization, invitations, invited, labelNames,
          memberships, name, pinned, powerUps, prefs, shortLink, shortUrl, starred,
          subscribed or url'
      - in: path
        name: idAction
        description: idAction
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Actions
      - Board
  /actions/{idAction}/board/{field}:
    get:
      summary: Get Actions Board Field
      description: Get actions board field.
      operationId: getActionsBoardByIdActionByField
      x-api-path-slug: actionsidactionboardfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idAction
        description: idAction
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Actions
      - Board
      - Field
  /actions/{idAction}/card:
    get:
      summary: Get Actions Card
      description: Get actions card.
      operationId: getActionsCardByIdAction
      x-api-path-slug: actionsidactioncard-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: badges, checkItemStates, closed,
          dateLastActivity, desc, descData, due, email, idAttachmentCover, idBoard,
          idChecklists, idLabels, idList, idMembers, idMembersVoted, idShort, labels,
          manualCoverAttachment, name, pos, shortLink, shortUrl, subscribed or url'
      - in: path
        name: idAction
        description: idAction
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Actions
      - Card
  /actions/{idAction}/card/{field}:
    get:
      summary: Get Actions Card Field
      description: Get actions card field.
      operationId: getActionsCardByIdActionByField
      x-api-path-slug: actionsidactioncardfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idAction
        description: idAction
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Actions
      - Card
      - Field
  /actions/{idAction}/display:
    get:
      summary: Get Actions Display
      description: Get actions display.
      operationId: getActionsDisplayByIdAction
      x-api-path-slug: actionsidactiondisplay-get
      parameters:
      - in: path
        name: idAction
        description: idAction
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Actions
      - Display
  /actions/{idAction}/entities:
    get:
      summary: Get Actions Entities
      description: Get actions entities.
      operationId: getActionsEntitiesByIdAction
      x-api-path-slug: actionsidactionentities-get
      parameters:
      - in: path
        name: idAction
        description: idAction
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Actions
      - Entities
  /actions/{idAction}/list:
    get:
      summary: Get Actions List
      description: Get actions list.
      operationId: getActionsListByIdAction
      x-api-path-slug: actionsidactionlist-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: closed, idBoard, name, pos
          or subscribed'
      - in: path
        name: idAction
        description: idAction
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Actions
      - List
  /actions/{idAction}/list/{field}:
    get:
      summary: Get Actions List Field
      description: Get actions list field.
      operationId: getActionsListByIdActionByField
      x-api-path-slug: actionsidactionlistfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idAction
        description: idAction
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Actions
      - List
      - Field
  /actions/{idAction}/member:
    get:
      summary: Get Actions Member
      description: Get actions member.
      operationId: getActionsMemberByIdAction
      x-api-path-slug: actionsidactionmember-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: avatarHash, avatarSource,
          bio, bioData, confirmed, email, fullName, gravatarHash, idBoards, idBoardsPinned,
          idOrganizations, idPremOrgsAdmin, initials, loginTypes, memberType, oneTimeMessagesDismissed,
          prefs, premiumFeatures, products, status, status, trophies, uploadedAvatarHash,
          url or username'
      - in: path
        name: idAction
        description: idAction
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Actions
      - Member
  /actions/{idAction}/member/{field}:
    get:
      summary: Get Actions Member Field
      description: Get actions member field.
      operationId: getActionsMemberByIdActionByField
      x-api-path-slug: actionsidactionmemberfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idAction
        description: idAction
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Actions
      - Member
      - Field
  /actions/{idAction}/memberCreator:
    get:
      summary: Get Actions Member Creator
      description: Get actions member creator.
      operationId: getActionsMemberCreatorByIdAction
      x-api-path-slug: actionsidactionmembercreator-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: avatarHash, avatarSource,
          bio, bioData, confirmed, email, fullName, gravatarHash, idBoards, idBoardsPinned,
          idOrganizations, idPremOrgsAdmin, initials, loginTypes, memberType, oneTimeMessagesDismissed,
          prefs, premiumFeatures, products, status, status, trophies, uploadedAvatarHash,
          url or username'
      - in: path
        name: idAction
        description: idAction
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Actions
      - Member
      - Creator
  /actions/{idAction}/memberCreator/{field}:
    get:
      summary: Get Actions Member Creator Field
      description: Get actions member creator field.
      operationId: getActionsMemberCreatorByIdActionByField
      x-api-path-slug: actionsidactionmembercreatorfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idAction
        description: idAction
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Actions
      - Member
      - Creator
      - Field
  /actions/{idAction}/organization:
    get:
      summary: Get Actions Organization
      description: Get actions organization.
      operationId: getActionsOrganizationByIdAction
      x-api-path-slug: actionsidactionorganization-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: billableMemberCount, desc,
          descData, displayName, idBoards, invitations, invited, logoHash, memberships,
          name, powerUps, prefs, premiumFeatures, products, url or website'
      - in: path
        name: idAction
        description: idAction
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Actions
      - Organization
  /actions/{idAction}/organization/{field}:
    get:
      summary: Get Actions Organization Field
      description: Get actions organization field.
      operationId: getActionsOrganizationByIdActionByField
      x-api-path-slug: actionsidactionorganizationfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idAction
        description: idAction
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Actions
      - Organization
      - Field
  /actions/{idAction}/text:
    put:
      summary: Put Actions Text
      description: Put actions text.
      operationId: updateActionsTextByIdAction
      x-api-path-slug: actionsidactiontext-put
      parameters:
      - in: body
        name: body
        description: Attributes of Actions Text to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idAction
        description: idAction
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Actions
      - Text
  /actions/{idAction}/{field}:
    get:
      summary: Get Actions Field
      description: Get actions field.
      operationId: getActionsByIdActionByField
      x-api-path-slug: actionsidactionfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idAction
        description: idAction
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Actions
      - Field
  /batch:
    get:
      summary: Get Batch
      description: Get batch.
      operationId: getBatch
      x-api-path-slug: batch-get
      parameters:
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      - in: query
        name: urls
        description: list of API v1 GET routes, not including the version prefix
      responses:
        200:
          description: OK
      tags:
      - Batch
  /boards:
    post:
      summary: Post Boards
      description: Post boards.
      operationId: addBoards
      x-api-path-slug: boards-post
      parameters:
      - in: body
        name: body
        description: Attributes of Boards to be added
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
  /boards/{idBoard}:
    get:
      summary: Get Boards
      description: Get boards.
      operationId: getBoardsByIdBoard
      x-api-path-slug: boardsidboard-get
      parameters:
      - in: query
        name: actions
        description: 'all or a comma-separated list of: addAttachmentToCard, addChecklistToCard,
          addMemberToBoard, addMemberToCard, addMemberToOrganization, addToOrganizationBoard,
          commentCard, convertToCardFromCheckItem, copyBoard, copyCard, copyCommentCard,
          createBoard, createCard, createList, createOrganization, deleteAttachmentFromCard,
          deleteBoardInvitation, deleteCard, deleteOrganizationInvitation, disablePowerUp,
          emailCard, enablePowerUp, makeAdminOfBoard, makeNormalMemberOfBoard, makeNormalMemberOfOrganization,
          makeObserverOfBoard, memberJoinedTrello, moveCardFromBoard, moveCardToBoard,
          moveListFromBoard, moveListToBoard, removeChecklistFromCard, removeFromOrganizationBoard,
          removeMemberFromCard, unconfirmedBoardInvitation, unconfirmedOrganizationInvitation,
          updateBoard, updateCard, updateCard:closed, updateCard:desc, updateCard:idList,
          updateCard:name, updateCheckItemStateOnCard, updateChecklist, updateList,
          updateList:closed, updateList:name, updateMember or updateOrganization'
      - in: query
        name: actions_display
        description: true or false
      - in: query
        name: actions_entities
        description: true or false
      - in: query
        name: actions_format
        description: 'One of: count, list or minimal'
      - in: query
        name: actions_limit
        description: a number from 0 to 1000
      - in: query
        name: actions_since
        description: A date, null or lastView
      - in: query
        name: action_fields
        description: 'all or a comma-separated list of: data, date, idMemberCreator
          or type'
      - in: query
        name: action_member
        description: true or false
      - in: query
        name: action_memberCreator
        description: true or false
      - in: query
        name: action_memberCreator_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: action_member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: boardStars
        description: 'One of: mine or none'
      - in: query
        name: cards
        description: 'One of: all, closed, none, open or visible'
      - in: query
        name: card_attachments
        description: A boolean value or &quot;cover&quot; for only card cover attachments
      - in: query
        name: card_attachment_fields
        description: 'all or a comma-separated list of: bytes, date, edgeColor, idMember,
          isUpload, mimeType, name, previews or url'
      - in: query
        name: card_checklists
        description: 'One of: all or none'
      - in: query
        name: card_fields
        description: 'all or a comma-separated list of: badges, checkItemStates, closed,
          dateLastActivity, desc, descData, due, email, idAttachmentCover, idBoard,
          idChecklists, idLabels, idList, idMembers, idMembersVoted, idShort, labels,
          manualCoverAttachment, name, pos, shortLink, shortUrl, subscribed or url'
      - in: query
        name: card_stickers
        description: true or false
      - in: query
        name: checklists
        description: 'One of: all or none'
      - in: query
        name: checklist_fields
        description: 'all or a comma-separated list of: idBoard, idCard, name or pos'
      - in: query
        name: fields
        description: 'all or a comma-separated list of: closed, dateLastActivity,
          dateLastView, desc, descData, idOrganization, invitations, invited, labelNames,
          memberships, name, pinned, powerUps, prefs, shortLink, shortUrl, starred,
          subscribed or url'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: labels
        description: 'One of: all or none'
      - in: query
        name: labels_limit
        description: a number from 0 to 1000
      - in: query
        name: label_fields
        description: 'all or a comma-separated list of: color, idBoard, name or uses'
      - in: query
        name: lists
        description: 'One of: all, closed, none or open'
      - in: query
        name: list_fields
        description: 'all or a comma-separated list of: closed, idBoard, name, pos
          or subscribed'
      - in: query
        name: members
        description: 'One of: admins, all, none, normal or owners'
      - in: query
        name: memberships
        description: 'all or a comma-separated list of: active, admin, deactivated,
          me or normal'
      - in: query
        name: memberships_member
        description: true or false
      - in: query
        name: memberships_member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: membersInvited
        description: 'One of: admins, all, none, normal or owners'
      - in: query
        name: membersInvited_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: myPrefs
        description: true or false
      - in: query
        name: organization
        description: true or false
      - in: query
        name: organization_fields
        description: 'all or a comma-separated list of: billableMemberCount, desc,
          descData, displayName, idBoards, invitations, invited, logoHash, memberships,
          name, powerUps, prefs, premiumFeatures, products, url or website'
      - in: query
        name: organization_memberships
        description: 'all or a comma-separated list of: active, admin, deactivated,
          me or normal'
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
    put:
      summary: Put Boards
      description: Put boards.
      operationId: updateBoardsByIdBoard
      x-api-path-slug: boardsidboard-put
      parameters:
      - in: body
        name: body
        description: Attributes of Boards to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
  /boards/{idBoard}/actions:
    get:
      summary: Get Boards Actions
      description: Get boards actions.
      operationId: getBoardsActionsByIdBoard
      x-api-path-slug: boardsidboardactions-get
      parameters:
      - in: query
        name: before
        description: A date, or null
      - in: query
        name: display
        description: true or false
      - in: query
        name: entities
        description: true or false
      - in: query
        name: fields
        description: 'all or a comma-separated list of: data, date, idMemberCreator
          or type'
      - in: query
        name: filter
        description: 'all or a comma-separated list of: addAttachmentToCard, addChecklistToCard,
          addMemberToBoard, addMemberToCard, addMemberToOrganization, addToOrganizationBoard,
          commentCard, convertToCardFromCheckItem, copyBoard, copyCard, copyCommentCard,
          createBoard, createCard, createList, createOrganization, deleteAttachmentFromCard,
          deleteBoardInvitation, deleteCard, deleteOrganizationInvitation, disablePowerUp,
          emailCard, enablePowerUp, makeAdminOfBoard, makeNormalMemberOfBoard, makeNormalMemberOfOrganization,
          makeObserverOfBoard, memberJoinedTrello, moveCardFromBoard, moveCardToBoard,
          moveListFromBoard, moveListToBoard, removeChecklistFromCard, removeFromOrganizationBoard,
          removeMemberFromCard, unconfirmedBoardInvitation, unconfirmedOrganizationInvitation,
          updateBoard, updateCard, updateCard:closed, updateCard:desc, updateCard:idList,
          updateCard:name, updateCheckItemStateOnCard, updateChecklist, updateList,
          updateList:closed, updateList:name, updateMember or updateOrganization'
      - in: query
        name: format
        description: 'One of: count, list or minimal'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: idModels
        description: Only return actions related to these model ids
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: limit
        description: a number from 0 to 1000
      - in: query
        name: member
        description: true or false
      - in: query
        name: memberCreator
        description: true or false
      - in: query
        name: memberCreator_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: page
        description: Page * limit must be less than 1000
      - in: query
        name: since
        description: A date, null or lastView
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Actions
  /boards/{idBoard}/boardStars:
    get:
      summary: Get Boards Boardstars
      description: Get boards boardstars.
      operationId: getBoardsBoardStarsByIdBoard
      x-api-path-slug: boardsidboardboardstars-get
      parameters:
      - in: query
        name: filter
        description: 'One of: mine or none'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Boardstars
  /boards/{idBoard}/calendarKey/generate:
    post:
      summary: Post Boards Calendarkey Generate
      description: Post boards calendarkey generate.
      operationId: addBoardsCalendarKeyGenerateByIdBoard
      x-api-path-slug: boardsidboardcalendarkeygenerate-post
      parameters:
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Calendarkey
      - Generate
  /boards/{idBoard}/cards:
    get:
      summary: Get Boards Cards
      description: Get boards cards.
      operationId: getBoardsCardsByIdBoard
      x-api-path-slug: boardsidboardcards-get
      parameters:
      - in: query
        name: actions
        description: 'all or a comma-separated list of: addAttachmentToCard, addChecklistToCard,
          addMemberToBoard, addMemberToCard, addMemberToOrganization, addToOrganizationBoard,
          commentCard, convertToCardFromCheckItem, copyBoard, copyCard, copyCommentCard,
          createBoard, createCard, createList, createOrganization, deleteAttachmentFromCard,
          deleteBoardInvitation, deleteCard, deleteOrganizationInvitation, disablePowerUp,
          emailCard, enablePowerUp, makeAdminOfBoard, makeNormalMemberOfBoard, makeNormalMemberOfOrganization,
          makeObserverOfBoard, memberJoinedTrello, moveCardFromBoard, moveCardToBoard,
          moveListFromBoard, moveListToBoard, removeChecklistFromCard, removeFromOrganizationBoard,
          removeMemberFromCard, unconfirmedBoardInvitation, unconfirmedOrganizationInvitation,
          updateBoard, updateCard, updateCard:closed, updateCard:desc, updateCard:idList,
          updateCard:name, updateCheckItemStateOnCard, updateChecklist, updateList,
          updateList:closed, updateList:name, updateMember or updateOrganization'
      - in: query
        name: attachments
        description: A boolean value or &quot;cover&quot; for only card cover attachments
      - in: query
        name: attachment_fields
        description: 'all or a comma-separated list of: bytes, date, edgeColor, idMember,
          isUpload, mimeType, name, previews or url'
      - in: query
        name: before
        description: A date, or null
      - in: query
        name: checkItemStates
        description: true or false
      - in: query
        name: checklists
        description: 'One of: all or none'
      - in: query
        name: fields
        description: 'all or a comma-separated list of: badges, checkItemStates, closed,
          dateLastActivity, desc, descData, due, email, idAttachmentCover, idBoard,
          idChecklists, idLabels, idList, idMembers, idMembersVoted, idShort, labels,
          manualCoverAttachment, name, pos, shortLink, shortUrl, subscribed or url'
      - in: query
        name: filter
        description: 'One of: all, closed, none, open or visible'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: limit
        description: a number from 1 to 1000
      - in: query
        name: members
        description: true or false
      - in: query
        name: member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: since
        description: A date, or null
      - in: query
        name: stickers
        description: true or false
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Cards
  /boards/{idBoard}/cards/{filter}:
    get:
      summary: Get Boards Cards Filter
      description: Get boards cards filter.
      operationId: getBoardsCardsByIdBoardByFilter
      x-api-path-slug: boardsidboardcardsfilter-get
      parameters:
      - in: path
        name: filter
        description: filter
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Cards
      - Filter
  /boards/{idBoard}/cards/{idCard}:
    get:
      summary: Get Boards Cards
      description: Get boards cards.
      operationId: getBoardsCardsByIdBoardByIdCard
      x-api-path-slug: boardsidboardcardsidcard-get
      parameters:
      - in: query
        name: actions
        description: 'all or a comma-separated list of: addAttachmentToCard, addChecklistToCard,
          addMemberToBoard, addMemberToCard, addMemberToOrganization, addToOrganizationBoard,
          commentCard, convertToCardFromCheckItem, copyBoard, copyCard, copyCommentCard,
          createBoard, createCard, createList, createOrganization, deleteAttachmentFromCard,
          deleteBoardInvitation, deleteCard, deleteOrganizationInvitation, disablePowerUp,
          emailCard, enablePowerUp, makeAdminOfBoard, makeNormalMemberOfBoard, makeNormalMemberOfOrganization,
          makeObserverOfBoard, memberJoinedTrello, moveCardFromBoard, moveCardToBoard,
          moveListFromBoard, moveListToBoard, removeChecklistFromCard, removeFromOrganizationBoard,
          removeMemberFromCard, unconfirmedBoardInvitation, unconfirmedOrganizationInvitation,
          updateBoard, updateCard, updateCard:closed, updateCard:desc, updateCard:idList,
          updateCard:name, updateCheckItemStateOnCard, updateChecklist, updateList,
          updateList:closed, updateList:name, updateMember or updateOrganization'
      - in: query
        name: actions_display
        description: true or false
      - in: query
        name: actions_entities
        description: true or false
      - in: query
        name: actions_limit
        description: a number from 0 to 1000
      - in: query
        name: action_fields
        description: 'all or a comma-separated list of: data, date, idMemberCreator
          or type'
      - in: query
        name: action_memberCreator_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: attachments
        description: A boolean value or &quot;cover&quot; for only card cover attachments
      - in: query
        name: attachment_fields
        description: 'all or a comma-separated list of: bytes, date, edgeColor, idMember,
          isUpload, mimeType, name, previews or url'
      - in: query
        name: checkItemStates
        description: true or false
      - in: query
        name: checkItemState_fields
        description: 'all or a comma-separated list of: idCheckItem or state'
      - in: query
        name: checklists
        description: 'One of: all or none'
      - in: query
        name: checklist_fields
        description: 'all or a comma-separated list of: idBoard, idCard, name or pos'
      - in: query
        name: fields
        description: 'all or a comma-separated list of: badges, checkItemStates, closed,
          dateLastActivity, desc, descData, due, email, idAttachmentCover, idBoard,
          idChecklists, idLabels, idList, idMembers, idMembersVoted, idShort, labels,
          manualCoverAttachment, name, pos, shortLink, shortUrl, subscribed or url'
      - in: path
        name: idBoard
        description: board_id
      - in: path
        name: idCard
        description: idCard
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: labels
        description: true or false
      - in: query
        name: members
        description: true or false
      - in: query
        name: member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Cards
  /boards/{idBoard}/checklists:
    get:
      summary: Get Boards Checklists
      description: Get boards checklists.
      operationId: getBoardsChecklistsByIdBoard
      x-api-path-slug: boardsidboardchecklists-get
      parameters:
      - in: query
        name: cards
        description: 'One of: all, closed, none, open or visible'
      - in: query
        name: card_fields
        description: 'all or a comma-separated list of: badges, checkItemStates, closed,
          dateLastActivity, desc, descData, due, email, idAttachmentCover, idBoard,
          idChecklists, idLabels, idList, idMembers, idMembersVoted, idShort, labels,
          manualCoverAttachment, name, pos, shortLink, shortUrl, subscribed or url'
      - in: query
        name: checkItems
        description: 'One of: all or none'
      - in: query
        name: checkItem_fields
        description: 'all or a comma-separated list of: name, nameData, pos, state
          or type'
      - in: query
        name: fields
        description: 'all or a comma-separated list of: idBoard, idCard, name or pos'
      - in: query
        name: filter
        description: 'One of: all or none'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Checklists
    post:
      summary: Post Boards Checklists
      description: Post boards checklists.
      operationId: addBoardsChecklistsByIdBoard
      x-api-path-slug: boardsidboardchecklists-post
      parameters:
      - in: body
        name: body
        description: Attributes of Boards Checklists to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Checklists
  /boards/{idBoard}/closed:
    put:
      summary: Put Boards Closed
      description: Put boards closed.
      operationId: updateBoardsClosedByIdBoard
      x-api-path-slug: boardsidboardclosed-put
      parameters:
      - in: body
        name: body
        description: Attributes of Boards Closed to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Closed
  /boards/{idBoard}/deltas:
    get:
      summary: Get Boards Deltas
      description: Get boards deltas.
      operationId: getBoardsDeltasByIdBoard
      x-api-path-slug: boardsidboarddeltas-get
      parameters:
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: ixLastUpdate
        description: a number from -1 to Infinity
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: tags
        description: A valid tag for subscribing
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Deltas
  /boards/{idBoard}/desc:
    put:
      summary: Put Boards Desc
      description: Put boards desc.
      operationId: updateBoardsDescByIdBoard
      x-api-path-slug: boardsidboarddesc-put
      parameters:
      - in: body
        name: body
        description: Attributes of Boards Desc to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Desc
  /boards/{idBoard}/emailKey/generate:
    post:
      summary: Post Boards Emailkey Generate
      description: Post boards emailkey generate.
      operationId: addBoardsEmailKeyGenerateByIdBoard
      x-api-path-slug: boardsidboardemailkeygenerate-post
      parameters:
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Emailkey
      - Generate
  /boards/{idBoard}/idOrganization:
    put:
      summary: Put Boards Organization
      description: Put boards organization.
      operationId: updateBoardsIdOrganizationByIdBoard
      x-api-path-slug: boardsidboardidorganization-put
      parameters:
      - in: body
        name: body
        description: Attributes of Boards Id Organization to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Organization
  /boards/{idBoard}/labelNames/blue:
    put:
      summary: Put Boards Label Names Blue
      description: Put boards label names blue.
      operationId: updateBoardsLabelNamesBlueByIdBoard
      x-api-path-slug: boardsidboardlabelnamesblue-put
      parameters:
      - in: body
        name: body
        description: Attributes of Label Names Blue to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Label
      - Names
      - Blue
  /boards/{idBoard}/labelNames/green:
    put:
      summary: Put Boards Label Names Green
      description: Put boards label names green.
      operationId: updateBoardsLabelNamesGreenByIdBoard
      x-api-path-slug: boardsidboardlabelnamesgreen-put
      parameters:
      - in: body
        name: body
        description: Attributes of Label Names Green to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Label
      - Names
      - Green
  /boards/{idBoard}/labelNames/orange:
    put:
      summary: Put Boards Label Names Orange
      description: Put boards label names orange.
      operationId: updateBoardsLabelNamesOrangeByIdBoard
      x-api-path-slug: boardsidboardlabelnamesorange-put
      parameters:
      - in: body
        name: body
        description: Attributes of Label Names Orange to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Label
      - Names
      - Orange
  /boards/{idBoard}/labelNames/purple:
    put:
      summary: Put Boards Label Names Purple
      description: Put boards label names purple.
      operationId: updateBoardsLabelNamesPurpleByIdBoard
      x-api-path-slug: boardsidboardlabelnamespurple-put
      parameters:
      - in: body
        name: body
        description: Attributes of Label Names Purple to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Label
      - Names
      - Purple
  /boards/{idBoard}/labelNames/red:
    put:
      summary: Put Boards Label Names Red
      description: Put boards label names red.
      operationId: updateBoardsLabelNamesRedByIdBoard
      x-api-path-slug: boardsidboardlabelnamesred-put
      parameters:
      - in: body
        name: body
        description: Attributes of Label Names Red to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Label
      - Names
      - Red
  /boards/{idBoard}/labelNames/yellow:
    put:
      summary: Put Boards Label Names Yellow
      description: Put boards label names yellow.
      operationId: updateBoardsLabelNamesYellowByIdBoard
      x-api-path-slug: boardsidboardlabelnamesyellow-put
      parameters:
      - in: body
        name: body
        description: Attributes of Label Names Yellow to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Label
      - Names
      - Yellow
  /boards/{idBoard}/labels:
    get:
      summary: Get Boards Labels
      description: Get boards labels.
      operationId: getBoardsLabelsByIdBoard
      x-api-path-slug: boardsidboardlabels-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: color, idBoard, name or uses'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: limit
        description: a number from 0 to 1000
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Labels
    post:
      summary: Post Boards Labels
      description: Post boards labels.
      operationId: addBoardsLabelsByIdBoard
      x-api-path-slug: boardsidboardlabels-post
      parameters:
      - in: body
        name: body
        description: Attributes of Boards Labels to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Labels
  /boards/{idBoard}/labels/{idLabel}:
    get:
      summary: Get Boards Labels Label
      description: Get boards labels label.
      operationId: getBoardsLabelsByIdBoardByIdLabel
      x-api-path-slug: boardsidboardlabelsidlabel-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: color, idBoard, name or uses'
      - in: path
        name: idBoard
        description: board_id
      - in: path
        name: idLabel
        description: idLabel
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Labels
      - Label
  /boards/{idBoard}/lists:
    get:
      summary: Get Boards Lists
      description: Get boards lists.
      operationId: getBoardsListsByIdBoard
      x-api-path-slug: boardsidboardlists-get
      parameters:
      - in: query
        name: cards
        description: 'One of: all, closed, none, open or visible'
      - in: query
        name: card_fields
        description: 'all or a comma-separated list of: badges, checkItemStates, closed,
          dateLastActivity, desc, descData, due, email, idAttachmentCover, idBoard,
          idChecklists, idLabels, idList, idMembers, idMembersVoted, idShort, labels,
          manualCoverAttachment, name, pos, shortLink, shortUrl, subscribed or url'
      - in: query
        name: fields
        description: 'all or a comma-separated list of: closed, idBoard, name, pos
          or subscribed'
      - in: query
        name: filter
        description: 'One of: all, closed, none or open'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Lists
    post:
      summary: Post Boards Lists
      description: Post boards lists.
      operationId: addBoardsListsByIdBoard
      x-api-path-slug: boardsidboardlists-post
      parameters:
      - in: body
        name: body
        description: Attributes of Boards Lists to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Lists
  /boards/{idBoard}/lists/{filter}:
    get:
      summary: Get Boards Lists Filter
      description: Get boards lists filter.
      operationId: getBoardsListsByIdBoardByFilter
      x-api-path-slug: boardsidboardlistsfilter-get
      parameters:
      - in: path
        name: filter
        description: filter
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Lists
      - Filter
  /boards/{idBoard}/markAsViewed:
    post:
      summary: Post Boards Markasviewed
      description: Post boards markasviewed.
      operationId: addBoardsMarkAsViewedByIdBoard
      x-api-path-slug: boardsidboardmarkasviewed-post
      parameters:
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Markasviewed
  /boards/{idBoard}/members:
    get:
      summary: Get Boards Members
      description: Get boards members.
      operationId: getBoardsMembersByIdBoard
      x-api-path-slug: boardsidboardmembers-get
      parameters:
      - in: query
        name: activity
        description: true or false ; works for premium organizations only
      - in: query
        name: fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: filter
        description: 'One of: admins, all, none, normal or owners'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Members
    put:
      summary: Put Boards Members
      description: Put boards members.
      operationId: updateBoardsMembersByIdBoard
      x-api-path-slug: boardsidboardmembers-put
      parameters:
      - in: body
        name: body
        description: Attributes of Boards Members to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Members
  /boards/{idBoard}/members/{filter}:
    get:
      summary: Get Boards Members Filter
      description: Get boards members filter.
      operationId: getBoardsMembersByIdBoardByFilter
      x-api-path-slug: boardsidboardmembersfilter-get
      parameters:
      - in: path
        name: filter
        description: filter
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Members
      - Filter
  /boards/{idBoard}/members/{idMember}:
    delete:
      summary: Delete Boards Members
      description: Delete boards members.
      operationId: deleteBoardsMembersByIdBoardByIdMember
      x-api-path-slug: boardsidboardmembersidmember-delete
      parameters:
      - in: path
        name: idBoard
        description: board_id
      - in: path
        name: idMember
        description: idMember
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Members
    put:
      summary: Put Boards Members
      description: Put boards members.
      operationId: updateBoardsMembersByIdBoardByIdMember
      x-api-path-slug: boardsidboardmembersidmember-put
      parameters:
      - in: body
        name: body
        description: Attributes of Boards Members to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: path
        name: idMember
        description: idMember
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Members
  /boards/{idBoard}/members/{idMember}/cards:
    get:
      summary: Get Boards Members Cards
      description: Get boards members cards.
      operationId: getBoardsMembersCardsByIdBoardByIdMember
      x-api-path-slug: boardsidboardmembersidmembercards-get
      parameters:
      - in: query
        name: actions
        description: 'all or a comma-separated list of: addAttachmentToCard, addChecklistToCard,
          addMemberToBoard, addMemberToCard, addMemberToOrganization, addToOrganizationBoard,
          commentCard, convertToCardFromCheckItem, copyBoard, copyCard, copyCommentCard,
          createBoard, createCard, createList, createOrganization, deleteAttachmentFromCard,
          deleteBoardInvitation, deleteCard, deleteOrganizationInvitation, disablePowerUp,
          emailCard, enablePowerUp, makeAdminOfBoard, makeNormalMemberOfBoard, makeNormalMemberOfOrganization,
          makeObserverOfBoard, memberJoinedTrello, moveCardFromBoard, moveCardToBoard,
          moveListFromBoard, moveListToBoard, removeChecklistFromCard, removeFromOrganizationBoard,
          removeMemberFromCard, unconfirmedBoardInvitation, unconfirmedOrganizationInvitation,
          updateBoard, updateCard, updateCard:closed, updateCard:desc, updateCard:idList,
          updateCard:name, updateCheckItemStateOnCard, updateChecklist, updateList,
          updateList:closed, updateList:name, updateMember or updateOrganization'
      - in: query
        name: attachments
        description: A boolean value or &quot;cover&quot; for only card cover attachments
      - in: query
        name: attachment_fields
        description: 'all or a comma-separated list of: bytes, date, edgeColor, idMember,
          isUpload, mimeType, name, previews or url'
      - in: query
        name: board
        description: true or false
      - in: query
        name: board_fields
        description: 'all or a comma-separated list of: closed, dateLastActivity,
          dateLastView, desc, descData, idOrganization, invitations, invited, labelNames,
          memberships, name, pinned, powerUps, prefs, shortLink, shortUrl, starred,
          subscribed or url'
      - in: query
        name: checkItemStates
        description: true or false
      - in: query
        name: checklists
        description: 'One of: all or none'
      - in: query
        name: fields
        description: 'all or a comma-separated list of: badges, checkItemStates, closed,
          dateLastActivity, desc, descData, due, email, idAttachmentCover, idBoard,
          idChecklists, idLabels, idList, idMembers, idMembersVoted, idShort, labels,
          manualCoverAttachment, name, pos, shortLink, shortUrl, subscribed or url'
      - in: query
        name: filter
        description: 'One of: all, closed, none, open or visible'
      - in: path
        name: idBoard
        description: board_id
      - in: path
        name: idMember
        description: idMember
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: list
        description: true or false
      - in: query
        name: list_fields
        description: 'all or a comma-separated list of: closed, idBoard, name, pos
          or subscribed'
      - in: query
        name: members
        description: true or false
      - in: query
        name: member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Members
      - Cards
  /boards/{idBoard}/membersInvited:
    get:
      summary: Get Boards Membersinvited
      description: Get boards membersinvited.
      operationId: getBoardsMembersInvitedByIdBoard
      x-api-path-slug: boardsidboardmembersinvited-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: avatarHash, avatarSource,
          bio, bioData, confirmed, email, fullName, gravatarHash, idBoards, idBoardsPinned,
          idOrganizations, idPremOrgsAdmin, initials, loginTypes, memberType, oneTimeMessagesDismissed,
          prefs, premiumFeatures, products, status, status, trophies, uploadedAvatarHash,
          url or username'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Membersinvited
  /boards/{idBoard}/membersInvited/{field}:
    get:
      summary: Get Boards Membersinvited Field
      description: Get boards membersinvited field.
      operationId: getBoardsMembersInvitedByIdBoardByField
      x-api-path-slug: boardsidboardmembersinvitedfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Membersinvited
      - Field
  /boards/{idBoard}/memberships:
    get:
      summary: Get Boards Memberships
      description: Get boards memberships.
      operationId: getBoardsMembershipsByIdBoard
      x-api-path-slug: boardsidboardmemberships-get
      parameters:
      - in: query
        name: filter
        description: 'all or a comma-separated list of: active, admin, deactivated,
          me or normal'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: member
        description: true or false
      - in: query
        name: member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Memberships
  /boards/{idBoard}/memberships/{idMembership}:
    get:
      summary: Get Boards Memberships
      description: Get boards memberships.
      operationId: getBoardsMembershipsByIdBoardByIdMembership
      x-api-path-slug: boardsidboardmembershipsidmembership-get
      parameters:
      - in: path
        name: idBoard
        description: board_id
      - in: path
        name: idMembership
        description: idMembership
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: member
        description: true or false
      - in: query
        name: member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Memberships
    put:
      summary: Put Boards Memberships
      description: Put boards memberships.
      operationId: updateBoardsMembershipsByIdBoardByIdMembership
      x-api-path-slug: boardsidboardmembershipsidmembership-put
      parameters:
      - in: body
        name: body
        description: Attributes of Boards Memberships to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: path
        name: idMembership
        description: idMembership
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Memberships
  /boards/{idBoard}/myPrefs:
    get:
      summary: Get Boards My Preferences
      description: Get boards my preferences.
      operationId: getBoardsMyPrefsByIdBoard
      x-api-path-slug: boardsidboardmyprefs-get
      parameters:
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - My
      - Preferences
  /boards/{idBoard}/myPrefs/emailPosition:
    put:
      summary: Put Boards My Preferences Emailposition
      description: Put boards my preferences emailposition.
      operationId: updateBoardsMyPrefsEmailPositionByIdBoard
      x-api-path-slug: boardsidboardmyprefsemailposition-put
      parameters:
      - in: body
        name: body
        description: Attributes of My Prefs Email Position to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - My
      - Preferences
      - Emailposition
  /boards/{idBoard}/myPrefs/idEmailList:
    put:
      summary: Put Boards My Preferences Emaillist
      description: Put boards my preferences emaillist.
      operationId: updateBoardsMyPrefsIdEmailListByIdBoard
      x-api-path-slug: boardsidboardmyprefsidemaillist-put
      parameters:
      - in: body
        name: body
        description: Attributes of My Prefs Id Email List to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - My
      - Preferences
      - Emaillist
  /boards/{idBoard}/myPrefs/showListGuide:
    put:
      summary: Put Boards My Preferences Showlistgue
      description: Put boards my preferences showlistgue.
      operationId: updateBoardsMyPrefsShowListGuideByIdBoard
      x-api-path-slug: boardsidboardmyprefsshowlistguide-put
      parameters:
      - in: body
        name: body
        description: Attributes of My Prefs Show List Guide to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - My
      - Preferences
      - Showlistgue
  /boards/{idBoard}/myPrefs/showSidebar:
    put:
      summary: Put Boards My Preferences Show Sidebar
      description: Put boards my preferences show sidebar.
      operationId: updateBoardsMyPrefsShowSidebarByIdBoard
      x-api-path-slug: boardsidboardmyprefsshowsidebar-put
      parameters:
      - in: body
        name: body
        description: Attributes of My Prefs Show Sidebar to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - My
      - Preferences
      - Show
      - Sidebar
  /boards/{idBoard}/myPrefs/showSidebarActivity:
    put:
      summary: Put Boards My Preferences Show Sidebar Activity
      description: Put boards my preferences show sidebar activity.
      operationId: updateBoardsMyPrefsShowSidebarActivityByIdBoard
      x-api-path-slug: boardsidboardmyprefsshowsidebaractivity-put
      parameters:
      - in: body
        name: body
        description: Attributes of My Prefs Show Sidebar Activity to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - My
      - Preferences
      - Show
      - Sidebar
      - Activity
  /boards/{idBoard}/myPrefs/showSidebarBoardActions:
    put:
      summary: Put Boards My Preferences Show Sidebar Board Actions
      description: Put boards my preferences show sidebar board actions.
      operationId: updateBoardsMyPrefsShowSidebarBoardActionsByIdBoard
      x-api-path-slug: boardsidboardmyprefsshowsidebarboardactions-put
      parameters:
      - in: body
        name: body
        description: Attributes of My Prefs Show Sidebar Board Actions to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - My
      - Preferences
      - Show
      - Sidebar
      - Board
      - Actions
  /boards/{idBoard}/myPrefs/showSidebarMembers:
    put:
      summary: Put Boards My Preferences Show Sidebarmembers
      description: Put boards my preferences show sidebarmembers.
      operationId: updateBoardsMyPrefsShowSidebarMembersByIdBoard
      x-api-path-slug: boardsidboardmyprefsshowsidebarmembers-put
      parameters:
      - in: body
        name: body
        description: Attributes of My Prefs Show Sidebar Members to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - My
      - Preferences
      - Show
      - Sidebarmembers
  /boards/{idBoard}/name:
    put:
      summary: Put Boards Name
      description: Put boards name.
      operationId: updateBoardsNameByIdBoard
      x-api-path-slug: boardsidboardname-put
      parameters:
      - in: body
        name: body
        description: Attributes of Boards Name to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Name
  /boards/{idBoard}/organization:
    get:
      summary: Get Boards Organization
      description: Get boards organization.
      operationId: getBoardsOrganizationByIdBoard
      x-api-path-slug: boardsidboardorganization-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: billableMemberCount, desc,
          descData, displayName, idBoards, invitations, invited, logoHash, memberships,
          name, powerUps, prefs, premiumFeatures, products, url or website'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Organization
  /boards/{idBoard}/organization/{field}:
    get:
      summary: Get Boards Organization Field
      description: Get boards organization field.
      operationId: getBoardsOrganizationByIdBoardByField
      x-api-path-slug: boardsidboardorganizationfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Organization
      - Field
  /boards/{idBoard}/powerUps:
    post:
      summary: Post Boards Powerups
      description: Post boards powerups.
      operationId: addBoardsPowerUpsByIdBoard
      x-api-path-slug: boardsidboardpowerups-post
      parameters:
      - in: body
        name: body
        description: Attributes of Boards Power Ups to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Powerups
  /boards/{idBoard}/powerUps/{powerUp}:
    delete:
      summary: Delete Boards Powerups Powerup
      description: Delete boards powerups powerup.
      operationId: deleteBoardsPowerUpsByIdBoardByPowerUp
      x-api-path-slug: boardsidboardpowerupspowerup-delete
      parameters:
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: path
        name: powerUp
        description: powerUp
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Powerups
      - Powerup
  /boards/{idBoard}/prefs/background:
    put:
      summary: Put Boards Preferences Background
      description: Put boards preferences background.
      operationId: updateBoardsPrefsBackgroundByIdBoard
      x-api-path-slug: boardsidboardprefsbackground-put
      parameters:
      - in: body
        name: body
        description: Attributes of Prefs Background to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Preferences
      - Background
  /boards/{idBoard}/prefs/calendarFeedEnabled:
    put:
      summary: Put Boards Preferences Calendar Feed Enabled
      description: Put boards preferences calendar feed enabled.
      operationId: updateBoardsPrefsCalendarFeedEnabledByIdBoard
      x-api-path-slug: boardsidboardprefscalendarfeedenabled-put
      parameters:
      - in: body
        name: body
        description: Attributes of Prefs Calendar Feed Enabled to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Preferences
      - Calendar
      - Feed
      - Enabled
  /boards/{idBoard}/prefs/cardAging:
    put:
      summary: Put Boards Preferences Cardaging
      description: Put boards preferences cardaging.
      operationId: updateBoardsPrefsCardAgingByIdBoard
      x-api-path-slug: boardsidboardprefscardaging-put
      parameters:
      - in: body
        name: body
        description: Attributes of Prefs Card Aging to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Preferences
      - Cardaging
  /boards/{idBoard}/prefs/cardCovers:
    put:
      summary: Put Boards Preferences Cardcovers
      description: Put boards preferences cardcovers.
      operationId: updateBoardsPrefsCardCoversByIdBoard
      x-api-path-slug: boardsidboardprefscardcovers-put
      parameters:
      - in: body
        name: body
        description: Attributes of Prefs Card Covers to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Preferences
      - Cardcovers
  /boards/{idBoard}/prefs/comments:
    put:
      summary: Put Boards Preferences Comments
      description: Put boards preferences comments.
      operationId: updateBoardsPrefsCommentsByIdBoard
      x-api-path-slug: boardsidboardprefscomments-put
      parameters:
      - in: body
        name: body
        description: Attributes of Prefs Comments to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Preferences
      - Comments
  /boards/{idBoard}/prefs/invitations:
    put:
      summary: Put Boards Preferences Invitations
      description: Put boards preferences invitations.
      operationId: updateBoardsPrefsInvitationsByIdBoard
      x-api-path-slug: boardsidboardprefsinvitations-put
      parameters:
      - in: body
        name: body
        description: Attributes of Prefs Invitations to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Preferences
      - Invitations
  /boards/{idBoard}/prefs/permissionLevel:
    put:
      summary: Put Boards Preferences Permissionlevel
      description: Put boards preferences permissionlevel.
      operationId: updateBoardsPrefsPermissionLevelByIdBoard
      x-api-path-slug: boardsidboardprefspermissionlevel-put
      parameters:
      - in: body
        name: body
        description: Attributes of Prefs Permission Level to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Preferences
      - Permissionlevel
  /boards/{idBoard}/prefs/selfJoin:
    put:
      summary: Put Boards Preferences Selfjoin
      description: Put boards preferences selfjoin.
      operationId: updateBoardsPrefsSelfJoinByIdBoard
      x-api-path-slug: boardsidboardprefsselfjoin-put
      parameters:
      - in: body
        name: body
        description: Attributes of Prefs Self Join to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Preferences
      - Selfjoin
  /boards/{idBoard}/prefs/voting:
    put:
      summary: Put Boards Preferences Voting
      description: Put boards preferences voting.
      operationId: updateBoardsPrefsVotingByIdBoard
      x-api-path-slug: boardsidboardprefsvoting-put
      parameters:
      - in: body
        name: body
        description: Attributes of Prefs Voting to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Preferences
      - Voting
  /boards/{idBoard}/subscribed:
    put:
      summary: Put Boards Subscribed
      description: Put boards subscribed.
      operationId: updateBoardsSubscribedByIdBoard
      x-api-path-slug: boardsidboardsubscribed-put
      parameters:
      - in: body
        name: body
        description: Attributes of Boards Subscribed to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Subscribed
  /boards/{idBoard}/{field}:
    get:
      summary: Get Boards Field
      description: Get boards field.
      operationId: getBoardsByIdBoardByField
      x-api-path-slug: boardsidboardfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Field
  /cards:
    post:
      summary: Post Cards
      description: Post cards.
      operationId: addCards
      x-api-path-slug: cards-post
      parameters:
      - in: body
        name: body
        description: Attributes of Cards to be added
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
  /cards/{idCard}:
    delete:
      summary: Delete Cards
      description: Delete cards.
      operationId: deleteCardsByIdCard
      x-api-path-slug: cardsidcard-delete
      parameters:
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
    get:
      summary: Get Cards
      description: Get cards.
      operationId: getCardsByIdCard
      x-api-path-slug: cardsidcard-get
      parameters:
      - in: query
        name: actions
        description: 'all or a comma-separated list of: addAttachmentToCard, addChecklistToCard,
          addMemberToBoard, addMemberToCard, addMemberToOrganization, addToOrganizationBoard,
          commentCard, convertToCardFromCheckItem, copyBoard, copyCard, copyCommentCard,
          createBoard, createCard, createList, createOrganization, deleteAttachmentFromCard,
          deleteBoardInvitation, deleteCard, deleteOrganizationInvitation, disablePowerUp,
          emailCard, enablePowerUp, makeAdminOfBoard, makeNormalMemberOfBoard, makeNormalMemberOfOrganization,
          makeObserverOfBoard, memberJoinedTrello, moveCardFromBoard, moveCardToBoard,
          moveListFromBoard, moveListToBoard, removeChecklistFromCard, removeFromOrganizationBoard,
          removeMemberFromCard, unconfirmedBoardInvitation, unconfirmedOrganizationInvitation,
          updateBoard, updateCard, updateCard:closed, updateCard:desc, updateCard:idList,
          updateCard:name, updateCheckItemStateOnCard, updateChecklist, updateList,
          updateList:closed, updateList:name, updateMember or updateOrganization'
      - in: query
        name: actions_display
        description: true or false
      - in: query
        name: actions_entities
        description: true or false
      - in: query
        name: actions_limit
        description: a number from 0 to 1000
      - in: query
        name: action_fields
        description: 'all or a comma-separated list of: data, date, idMemberCreator
          or type'
      - in: query
        name: action_memberCreator_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: attachments
        description: A boolean value or &quot;cover&quot; for only card cover attachments
      - in: query
        name: attachment_fields
        description: 'all or a comma-separated list of: bytes, date, edgeColor, idMember,
          isUpload, mimeType, name, previews or url'
      - in: query
        name: board
        description: true or false
      - in: query
        name: board_fields
        description: 'all or a comma-separated list of: closed, dateLastActivity,
          dateLastView, desc, descData, idOrganization, invitations, invited, labelNames,
          memberships, name, pinned, powerUps, prefs, shortLink, shortUrl, starred,
          subscribed or url'
      - in: query
        name: checkItemStates
        description: true or false
      - in: query
        name: checkItemState_fields
        description: 'all or a comma-separated list of: idCheckItem or state'
      - in: query
        name: checklists
        description: 'One of: all or none'
      - in: query
        name: checklist_fields
        description: 'all or a comma-separated list of: idBoard, idCard, name or pos'
      - in: query
        name: fields
        description: 'all or a comma-separated list of: badges, checkItemStates, closed,
          dateLastActivity, desc, descData, due, email, idAttachmentCover, idBoard,
          idChecklists, idLabels, idList, idMembers, idMembersVoted, idShort, labels,
          manualCoverAttachment, name, pos, shortLink, shortUrl, subscribed or url'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: list
        description: true or false
      - in: query
        name: list_fields
        description: 'all or a comma-separated list of: closed, idBoard, name, pos
          or subscribed'
      - in: query
        name: members
        description: true or false
      - in: query
        name: membersVoted
        description: true or false
      - in: query
        name: memberVoted_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: stickers
        description: true or false
      - in: query
        name: sticker_fields
        description: 'all or a comma-separated list of: image, imageScaled, imageUrl,
          left, rotate, top or zIndex'
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
    put:
      summary: Put Cards
      description: Put cards.
      operationId: updateCardsByIdCard
      x-api-path-slug: cardsidcard-put
      parameters:
      - in: body
        name: body
        description: Attributes of Cards to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
  /cards/{idCard}/actions:
    get:
      summary: Get Cards Actions
      description: Get cards actions.
      operationId: getCardsActionsByIdCard
      x-api-path-slug: cardsidcardactions-get
      parameters:
      - in: query
        name: before
        description: A date, or null
      - in: query
        name: display
        description: true or false
      - in: query
        name: entities
        description: true or false
      - in: query
        name: fields
        description: 'all or a comma-separated list of: data, date, idMemberCreator
          or type'
      - in: query
        name: filter
        description: 'all or a comma-separated list of: addAttachmentToCard, addChecklistToCard,
          addMemberToBoard, addMemberToCard, addMemberToOrganization, addToOrganizationBoard,
          commentCard, convertToCardFromCheckItem, copyBoard, copyCard, copyCommentCard,
          createBoard, createCard, createList, createOrganization, deleteAttachmentFromCard,
          deleteBoardInvitation, deleteCard, deleteOrganizationInvitation, disablePowerUp,
          emailCard, enablePowerUp, makeAdminOfBoard, makeNormalMemberOfBoard, makeNormalMemberOfOrganization,
          makeObserverOfBoard, memberJoinedTrello, moveCardFromBoard, moveCardToBoard,
          moveListFromBoard, moveListToBoard, removeChecklistFromCard, removeFromOrganizationBoard,
          removeMemberFromCard, unconfirmedBoardInvitation, unconfirmedOrganizationInvitation,
          updateBoard, updateCard, updateCard:closed, updateCard:desc, updateCard:idList,
          updateCard:name, updateCheckItemStateOnCard, updateChecklist, updateList,
          updateList:closed, updateList:name, updateMember or updateOrganization'
      - in: query
        name: format
        description: 'One of: count, list or minimal'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: idModels
        description: Only return actions related to these model ids
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: limit
        description: a number from 0 to 1000
      - in: query
        name: member
        description: true or false
      - in: query
        name: memberCreator
        description: true or false
      - in: query
        name: memberCreator_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: page
        description: Page * limit must be less than 1000
      - in: query
        name: since
        description: A date, null or lastView
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Actions
  /cards/{idCard}/actions/comments:
    post:
      summary: Post Cards Actions Comments
      description: Post cards actions comments.
      operationId: addCardsActionsCommentsByIdCard
      x-api-path-slug: cardsidcardactionscomments-post
      parameters:
      - in: body
        name: body
        description: Attributes of Actions Comments to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Actions
      - Comments
  /cards/{idCard}/actions/{idAction}/comments:
    delete:
      summary: Delete Cards Actions Comments
      description: Delete cards actions comments.
      operationId: deleteCardsActionsCommentsByIdCardByIdAction
      x-api-path-slug: cardsidcardactionsidactioncomments-delete
      parameters:
      - in: path
        name: idAction
        description: idAction
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Actions
      - Comments
    put:
      summary: Put Cards Actions Comments
      description: Put cards actions comments.
      operationId: updateCardsActionsCommentsByIdCardByIdAction
      x-api-path-slug: cardsidcardactionsidactioncomments-put
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Actions Comments to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idAction
        description: idAction
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Actions
      - Comments
  /cards/{idCard}/attachments:
    get:
      summary: Get Cards Attachments
      description: Get cards attachments.
      operationId: getCardsAttachmentsByIdCard
      x-api-path-slug: cardsidcardattachments-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: bytes, date, edgeColor, idMember,
          isUpload, mimeType, name, previews or url'
      - in: query
        name: filter
        description: A boolean value or &quot;cover&quot; for only card cover attachments
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Attachments
    post:
      summary: Post Cards Attachments
      description: Post cards attachments.
      operationId: addCardsAttachmentsByIdCard
      x-api-path-slug: cardsidcardattachments-post
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Attachments to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Attachments
  /cards/{idCard}/attachments/{idAttachment}:
    delete:
      summary: Delete Cards Attachments Attachment
      description: Delete cards attachments attachment.
      operationId: deleteCardsAttachmentsByIdCardByIdAttachment
      x-api-path-slug: cardsidcardattachmentsidattachment-delete
      parameters:
      - in: path
        name: idAttachment
        description: idAttachment
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Attachments
      - Attachment
    get:
      summary: Get Cards Attachments Attachment
      description: Get cards attachments attachment.
      operationId: getCardsAttachmentsByIdCardByIdAttachment
      x-api-path-slug: cardsidcardattachmentsidattachment-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: bytes, date, edgeColor, idMember,
          isUpload, mimeType, name, previews or url'
      - in: path
        name: idAttachment
        description: idAttachment
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Attachments
      - Attachment
  /cards/{idCard}/board:
    get:
      summary: Get Cards Board
      description: Get cards board.
      operationId: getCardsBoardByIdCard
      x-api-path-slug: cardsidcardboard-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: closed, dateLastActivity,
          dateLastView, desc, descData, idOrganization, invitations, invited, labelNames,
          memberships, name, pinned, powerUps, prefs, shortLink, shortUrl, starred,
          subscribed or url'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Board
  /cards/{idCard}/board/{field}:
    get:
      summary: Get Cards Board Field
      description: Get cards board field.
      operationId: getCardsBoardByIdCardByField
      x-api-path-slug: cardsidcardboardfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Board
      - Field
  /cards/{idCard}/checkItemStates:
    get:
      summary: Get Cards Checkitemstates
      description: Get cards checkitemstates.
      operationId: getCardsCheckItemStatesByIdCard
      x-api-path-slug: cardsidcardcheckitemstates-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: idCheckItem or state'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Checkitemstates
  /cards/{idCard}/checklist/{idChecklistCurrent}/checkItem/{idCheckItem}:
    put:
      summary: Put Cards Checklistcurrent Checkitem Checkitem
      description: Put cards checklistcurrent checkitem checkitem.
      operationId: updateCardsChecklistCheckItemByIdCardByIdChecklistCurrentByIdCheckItem
      x-api-path-slug: cardsidcardchecklistidchecklistcurrentcheckitemidcheckitem-put
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Checklist Id Checklist Current Check Item
          to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: path
        name: idCheckItem
        description: idCheckItem
      - in: path
        name: idChecklistCurrent
        description: idChecklistCurrent
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Checklistcurrent
      - Checkitem
      - Checkitem
  /cards/{idCard}/checklist/{idChecklist}/checkItem:
    post:
      summary: Post Cards Checklist Checkitem
      description: Post cards checklist checkitem.
      operationId: addCardsChecklistCheckItemByIdCardByIdChecklist
      x-api-path-slug: cardsidcardchecklistidchecklistcheckitem-post
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Checklist Check Item to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Checklist
      - Checkitem
  /cards/{idCard}/checklist/{idChecklist}/checkItem/{idCheckItem}:
    delete:
      summary: Delete Cards Checklist Checkitem Checkitem
      description: Delete cards checklist checkitem checkitem.
      operationId: deleteCardsChecklistCheckItemByIdCardByIdChecklistByIdCheckItem
      x-api-path-slug: cardsidcardchecklistidchecklistcheckitemidcheckitem-delete
      parameters:
      - in: path
        name: idCard
        description: card id or shortlink
      - in: path
        name: idCheckItem
        description: idCheckItem
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Checklist
      - Checkitem
      - Checkitem
  /cards/{idCard}/checklist/{idChecklist}/checkItem/{idCheckItem}/convertToCard:
    post:
      summary: Post Cards Checklist Checkitem Checkitem Converttocard
      description: Post cards checklist checkitem checkitem converttocard.
      operationId: addCardsChecklistCheckItemConvertToCardByIdCardByIdChecklistByIdCheckItem
      x-api-path-slug: cardsidcardchecklistidchecklistcheckitemidcheckitemconverttocard-post
      parameters:
      - in: path
        name: idCard
        description: card id or shortlink
      - in: path
        name: idCheckItem
        description: idCheckItem
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Checklist
      - Checkitem
      - Checkitem
      - Converttocard
  /cards/{idCard}/checklist/{idChecklist}/checkItem/{idCheckItem}/name:
    put:
      summary: Put Cards Checklist Checkitem Checkitem Name
      description: Put cards checklist checkitem checkitem name.
      operationId: updateCardsChecklistCheckItemNameByIdCardByIdChecklistByIdCheckItem
      x-api-path-slug: cardsidcardchecklistidchecklistcheckitemidcheckitemname-put
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Checklist Check Item Name to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: path
        name: idCheckItem
        description: idCheckItem
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Checklist
      - Checkitem
      - Checkitem
      - Name
  /cards/{idCard}/checklist/{idChecklist}/checkItem/{idCheckItem}/pos:
    put:
      summary: Put Cards Checklist Checkitem Checkitem Pos
      description: Put cards checklist checkitem checkitem pos.
      operationId: updateCardsChecklistCheckItemPosByIdCardByIdChecklistByIdCheckItem
      x-api-path-slug: cardsidcardchecklistidchecklistcheckitemidcheckitempos-put
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Checklist Check Item Pos to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: path
        name: idCheckItem
        description: idCheckItem
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Checklist
      - Checkitem
      - Checkitem
      - Pos
  /cards/{idCard}/checklist/{idChecklist}/checkItem/{idCheckItem}/state:
    put:
      summary: Put Cards Checklist Checkitem Checkitem State
      description: Put cards checklist checkitem checkitem state.
      operationId: updateCardsChecklistCheckItemStateByIdCardByIdChecklistByIdCheckItem
      x-api-path-slug: cardsidcardchecklistidchecklistcheckitemidcheckitemstate-put
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Checklist Check Item State to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: path
        name: idCheckItem
        description: idCheckItem
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Checklist
      - Checkitem
      - Checkitem
      - State
  /cards/{idCard}/checklists:
    get:
      summary: Get Cards Checklists
      description: Get cards checklists.
      operationId: getCardsChecklistsByIdCard
      x-api-path-slug: cardsidcardchecklists-get
      parameters:
      - in: query
        name: cards
        description: 'One of: all, closed, none, open or visible'
      - in: query
        name: card_fields
        description: 'all or a comma-separated list of: badges, checkItemStates, closed,
          dateLastActivity, desc, descData, due, email, idAttachmentCover, idBoard,
          idChecklists, idLabels, idList, idMembers, idMembersVoted, idShort, labels,
          manualCoverAttachment, name, pos, shortLink, shortUrl, subscribed or url'
      - in: query
        name: checkItems
        description: 'One of: all or none'
      - in: query
        name: checkItem_fields
        description: 'all or a comma-separated list of: name, nameData, pos, state
          or type'
      - in: query
        name: fields
        description: 'all or a comma-separated list of: idBoard, idCard, name or pos'
      - in: query
        name: filter
        description: 'One of: all or none'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Checklists
    post:
      summary: Post Cards Checklists
      description: Post cards checklists.
      operationId: addCardsChecklistsByIdCard
      x-api-path-slug: cardsidcardchecklists-post
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Checklists to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Checklists
  /cards/{idCard}/checklists/{idChecklist}:
    delete:
      summary: Delete Cards Checklists
      description: Delete cards checklists.
      operationId: deleteCardsChecklistsByIdCardByIdChecklist
      x-api-path-slug: cardsidcardchecklistsidchecklist-delete
      parameters:
      - in: path
        name: idCard
        description: card id or shortlink
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Checklists
  /cards/{idCard}/closed:
    put:
      summary: Put Cards Closed
      description: Put cards closed.
      operationId: updateCardsClosedByIdCard
      x-api-path-slug: cardsidcardclosed-put
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Closed to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Closed
  /cards/{idCard}/desc:
    put:
      summary: Put Cards Desc
      description: Put cards desc.
      operationId: updateCardsDescByIdCard
      x-api-path-slug: cardsidcarddesc-put
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Desc to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Desc
  /cards/{idCard}/due:
    put:
      summary: Put Cards Due
      description: Put cards due.
      operationId: updateCardsDueByIdCard
      x-api-path-slug: cardsidcarddue-put
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Due to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Due
  /cards/{idCard}/idAttachmentCover:
    put:
      summary: Put Cards Attachmentcover
      description: Put cards attachmentcover.
      operationId: updateCardsIdAttachmentCoverByIdCard
      x-api-path-slug: cardsidcardidattachmentcover-put
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Id Attachment Cover to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Attachmentcover
  /cards/{idCard}/idBoard:
    put:
      summary: Put Cards Board
      description: Put cards board.
      operationId: updateCardsIdBoardByIdCard
      x-api-path-slug: cardsidcardidboard-put
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Id Board to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Board
  /cards/{idCard}/idLabels:
    post:
      summary: Post Cards Labels
      description: Post cards labels.
      operationId: addCardsIdLabelsByIdCard
      x-api-path-slug: cardsidcardidlabels-post
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Id Labels to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Labels
  /cards/{idCard}/idLabels/{idLabel}:
    delete:
      summary: Delete Cards Labels Label
      description: Delete cards labels label.
      operationId: deleteCardsIdLabelsByIdCardByIdLabel
      x-api-path-slug: cardsidcardidlabelsidlabel-delete
      parameters:
      - in: path
        name: idCard
        description: card id or shortlink
      - in: path
        name: idLabel
        description: idLabel
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Labels
      - Label
  /cards/{idCard}/idList:
    put:
      summary: Put Cards List
      description: Put cards list.
      operationId: updateCardsIdListByIdCard
      x-api-path-slug: cardsidcardidlist-put
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Id List to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - List
  /cards/{idCard}/idMembers:
    post:
      summary: Post Cards Members
      description: Post cards members.
      operationId: addCardsIdMembersByIdCard
      x-api-path-slug: cardsidcardidmembers-post
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Id Members to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Members
    put:
      summary: Put Cards Members
      description: Put cards members.
      operationId: updateCardsIdMembersByIdCard
      x-api-path-slug: cardsidcardidmembers-put
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Id Members to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Members
  /cards/{idCard}/idMembers/{idMember}:
    delete:
      summary: Delete Cards Members
      description: Delete cards members.
      operationId: deleteCardsIdMembersByIdCardByIdMember
      x-api-path-slug: cardsidcardidmembersidmember-delete
      parameters:
      - in: path
        name: idCard
        description: card id or shortlink
      - in: path
        name: idMember
        description: idMember
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Members
  /cards/{idCard}/labels:
    post:
      summary: Post Cards Labels
      description: Post cards labels.
      operationId: addCardsLabelsByIdCard
      x-api-path-slug: cardsidcardlabels-post
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Labels to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Labels
    put:
      summary: Put Cards Labels
      description: Put cards labels.
      operationId: updateCardsLabelsByIdCard
      x-api-path-slug: cardsidcardlabels-put
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Labels to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Labels
  /cards/{idCard}/labels/{color}:
    delete:
      summary: Delete Cards Labels Color
      description: Delete cards labels color.
      operationId: deleteCardsLabelsByIdCardByColor
      x-api-path-slug: cardsidcardlabelscolor-delete
      parameters:
      - in: path
        name: color
        description: color
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Labels
      - Color
  /cards/{idCard}/list:
    get:
      summary: Get Cards List
      description: Get cards list.
      operationId: getCardsListByIdCard
      x-api-path-slug: cardsidcardlist-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: closed, idBoard, name, pos
          or subscribed'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - List
  /cards/{idCard}/list/{field}:
    get:
      summary: Get Cards List Field
      description: Get cards list field.
      operationId: getCardsListByIdCardByField
      x-api-path-slug: cardsidcardlistfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - List
      - Field
  /cards/{idCard}/markAssociatedNotificationsRead:
    post:
      summary: Post Cards Markassociatednotificationsread
      description: Post cards markassociatednotificationsread.
      operationId: addCardsMarkAssociatedNotificationsReadByIdCard
      x-api-path-slug: cardsidcardmarkassociatednotificationsread-post
      parameters:
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Markassociatednotificationsread
  /cards/{idCard}/members:
    get:
      summary: Get Cards Members
      description: Get cards members.
      operationId: getCardsMembersByIdCard
      x-api-path-slug: cardsidcardmembers-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Members
  /cards/{idCard}/membersVoted:
    get:
      summary: Get Cards Membersvoted
      description: Get cards membersvoted.
      operationId: getCardsMembersVotedByIdCard
      x-api-path-slug: cardsidcardmembersvoted-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Membersvoted
    post:
      summary: Post Cards Membersvoted
      description: Post cards membersvoted.
      operationId: addCardsMembersVotedByIdCard
      x-api-path-slug: cardsidcardmembersvoted-post
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Members Voted to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Membersvoted
  /cards/{idCard}/membersVoted/{idMember}:
    delete:
      summary: Delete Cards Membersvoted Member
      description: Delete cards membersvoted member.
      operationId: deleteCardsMembersVotedByIdCardByIdMember
      x-api-path-slug: cardsidcardmembersvotedidmember-delete
      parameters:
      - in: path
        name: idCard
        description: card id or shortlink
      - in: path
        name: idMember
        description: idMember
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Membersvoted
      - Member
  /cards/{idCard}/name:
    put:
      summary: Put Cards Name
      description: Put cards name.
      operationId: updateCardsNameByIdCard
      x-api-path-slug: cardsidcardname-put
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Name to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Name
  /cards/{idCard}/pos:
    put:
      summary: Put Cards Pos
      description: Put cards pos.
      operationId: updateCardsPosByIdCard
      x-api-path-slug: cardsidcardpos-put
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Pos to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Pos
  /cards/{idCard}/stickers:
    get:
      summary: Get Cards Stickers
      description: Get cards stickers.
      operationId: getCardsStickersByIdCard
      x-api-path-slug: cardsidcardstickers-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: image, imageScaled, imageUrl,
          left, rotate, top or zIndex'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Stickers
    post:
      summary: Post Cards Stickers
      description: Post cards stickers.
      operationId: addCardsStickersByIdCard
      x-api-path-slug: cardsidcardstickers-post
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Stickers to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Stickers
  /cards/{idCard}/stickers/{idSticker}:
    delete:
      summary: Delete Cards Stickers Sticker
      description: Delete cards stickers sticker.
      operationId: deleteCardsStickersByIdCardByIdSticker
      x-api-path-slug: cardsidcardstickersidsticker-delete
      parameters:
      - in: path
        name: idCard
        description: card id or shortlink
      - in: path
        name: idSticker
        description: idSticker
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Stickers
      - Sticker
    get:
      summary: Get Cards Stickers Sticker
      description: Get cards stickers sticker.
      operationId: getCardsStickersByIdCardByIdSticker
      x-api-path-slug: cardsidcardstickersidsticker-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: image, imageScaled, imageUrl,
          left, rotate, top or zIndex'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: path
        name: idSticker
        description: idSticker
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Stickers
      - Sticker
    put:
      summary: Put Cards Stickers Sticker
      description: Put cards stickers sticker.
      operationId: updateCardsStickersByIdCardByIdSticker
      x-api-path-slug: cardsidcardstickersidsticker-put
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Stickers to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: path
        name: idSticker
        description: idSticker
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Stickers
      - Sticker
  /cards/{idCard}/subscribed:
    put:
      summary: Put Cards Subscribed
      description: Put cards subscribed.
      operationId: updateCardsSubscribedByIdCard
      x-api-path-slug: cardsidcardsubscribed-put
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Subscribed to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Subscribed
  /cards/{idCard}/{field}:
    get:
      summary: Get Cards Field
      description: Get cards field.
      operationId: getCardsByIdCardByField
      x-api-path-slug: cardsidcardfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Field
  /checklists:
    post:
      summary: Post Checklists
      description: Post checklists.
      operationId: addChecklists
      x-api-path-slug: checklists-post
      parameters:
      - in: body
        name: body
        description: Attributes of Checklists to be added
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
  /checklists/{idChecklist}:
    delete:
      summary: Delete Checklists
      description: Delete checklists.
      operationId: deleteChecklistsByIdChecklist
      x-api-path-slug: checklistsidchecklist-delete
      parameters:
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
    get:
      summary: Get Checklists
      description: Get checklists.
      operationId: getChecklistsByIdChecklist
      x-api-path-slug: checklistsidchecklist-get
      parameters:
      - in: query
        name: cards
        description: 'One of: all, closed, none, open or visible'
      - in: query
        name: card_fields
        description: 'all or a comma-separated list of: badges, checkItemStates, closed,
          dateLastActivity, desc, descData, due, email, idAttachmentCover, idBoard,
          idChecklists, idLabels, idList, idMembers, idMembersVoted, idShort, labels,
          manualCoverAttachment, name, pos, shortLink, shortUrl, subscribed or url'
      - in: query
        name: checkItems
        description: 'One of: all or none'
      - in: query
        name: checkItem_fields
        description: 'all or a comma-separated list of: name, nameData, pos, state
          or type'
      - in: query
        name: fields
        description: 'all or a comma-separated list of: idBoard, idCard, name or pos'
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
    put:
      summary: Put Checklists
      description: Put checklists.
      operationId: updateChecklistsByIdChecklist
      x-api-path-slug: checklistsidchecklist-put
      parameters:
      - in: body
        name: body
        description: Attributes of Checklists to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
  /checklists/{idChecklist}/board:
    get:
      summary: Get Checklists Board
      description: Get checklists board.
      operationId: getChecklistsBoardByIdChecklist
      x-api-path-slug: checklistsidchecklistboard-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: closed, dateLastActivity,
          dateLastView, desc, descData, idOrganization, invitations, invited, labelNames,
          memberships, name, pinned, powerUps, prefs, shortLink, shortUrl, starred,
          subscribed or url'
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Board
  /checklists/{idChecklist}/board/{field}:
    get:
      summary: Get Checklists Board Field
      description: Get checklists board field.
      operationId: getChecklistsBoardByIdChecklistByField
      x-api-path-slug: checklistsidchecklistboardfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Board
      - Field
  /checklists/{idChecklist}/cards:
    get:
      summary: Get Checklists Cards
      description: Get checklists cards.
      operationId: getChecklistsCardsByIdChecklist
      x-api-path-slug: checklistsidchecklistcards-get
      parameters:
      - in: query
        name: actions
        description: 'all or a comma-separated list of: addAttachmentToCard, addChecklistToCard,
          addMemberToBoard, addMemberToCard, addMemberToOrganization, addToOrganizationBoard,
          commentCard, convertToCardFromCheckItem, copyBoard, copyCard, copyCommentCard,
          createBoard, createCard, createList, createOrganization, deleteAttachmentFromCard,
          deleteBoardInvitation, deleteCard, deleteOrganizationInvitation, disablePowerUp,
          emailCard, enablePowerUp, makeAdminOfBoard, makeNormalMemberOfBoard, makeNormalMemberOfOrganization,
          makeObserverOfBoard, memberJoinedTrello, moveCardFromBoard, moveCardToBoard,
          moveListFromBoard, moveListToBoard, removeChecklistFromCard, removeFromOrganizationBoard,
          removeMemberFromCard, unconfirmedBoardInvitation, unconfirmedOrganizationInvitation,
          updateBoard, updateCard, updateCard:closed, updateCard:desc, updateCard:idList,
          updateCard:name, updateCheckItemStateOnCard, updateChecklist, updateList,
          updateList:closed, updateList:name, updateMember or updateOrganization'
      - in: query
        name: attachments
        description: A boolean value or &quot;cover&quot; for only card cover attachments
      - in: query
        name: attachment_fields
        description: 'all or a comma-separated list of: bytes, date, edgeColor, idMember,
          isUpload, mimeType, name, previews or url'
      - in: query
        name: before
        description: A date, or null
      - in: query
        name: checkItemStates
        description: true or false
      - in: query
        name: checklists
        description: 'One of: all or none'
      - in: query
        name: fields
        description: 'all or a comma-separated list of: badges, checkItemStates, closed,
          dateLastActivity, desc, descData, due, email, idAttachmentCover, idBoard,
          idChecklists, idLabels, idList, idMembers, idMembersVoted, idShort, labels,
          manualCoverAttachment, name, pos, shortLink, shortUrl, subscribed or url'
      - in: query
        name: filter
        description: 'One of: all, closed, none or open'
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: limit
        description: a number from 1 to 1000
      - in: query
        name: members
        description: true or false
      - in: query
        name: member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: since
        description: A date, or null
      - in: query
        name: stickers
        description: true or false
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Cards
  /checklists/{idChecklist}/cards/{filter}:
    get:
      summary: Get Checklists Cards Filter
      description: Get checklists cards filter.
      operationId: getChecklistsCardsByIdChecklistByFilter
      x-api-path-slug: checklistsidchecklistcardsfilter-get
      parameters:
      - in: path
        name: filter
        description: filter
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Cards
      - Filter
  /checklists/{idChecklist}/checkItems:
    get:
      summary: Get Checklists Checkitems
      description: Get checklists checkitems.
      operationId: getChecklistsCheckItemsByIdChecklist
      x-api-path-slug: checklistsidchecklistcheckitems-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: name, nameData, pos, state
          or type'
      - in: query
        name: filter
        description: 'One of: all or none'
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Checkitems
    post:
      summary: Post Checklists Checkitems
      description: Post checklists checkitems.
      operationId: addChecklistsCheckItemsByIdChecklist
      x-api-path-slug: checklistsidchecklistcheckitems-post
      parameters:
      - in: body
        name: body
        description: Attributes of Checklists Check Items to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Checkitems
  /checklists/{idChecklist}/checkItems/{idCheckItem}:
    delete:
      summary: Delete Checklists Checkitems Checkitem
      description: Delete checklists checkitems checkitem.
      operationId: deleteChecklistsCheckItemsByIdChecklistByIdCheckItem
      x-api-path-slug: checklistsidchecklistcheckitemsidcheckitem-delete
      parameters:
      - in: path
        name: idCheckItem
        description: idCheckItem
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Checkitems
      - Checkitem
    get:
      summary: Get Checklists Checkitems Checkitem
      description: Get checklists checkitems checkitem.
      operationId: getChecklistsCheckItemsByIdChecklistByIdCheckItem
      x-api-path-slug: checklistsidchecklistcheckitemsidcheckitem-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: name, nameData, pos, state
          or type'
      - in: path
        name: idCheckItem
        description: idCheckItem
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Checkitems
      - Checkitem
  /checklists/{idChecklist}/idCard:
    put:
      summary: Put Checklists Card
      description: Put checklists card.
      operationId: updateChecklistsIdCardByIdChecklist
      x-api-path-slug: checklistsidchecklistidcard-put
      parameters:
      - in: body
        name: body
        description: Attributes of Checklists Id Card to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Card
  /checklists/{idChecklist}/name:
    put:
      summary: Put Checklists Name
      description: Put checklists name.
      operationId: updateChecklistsNameByIdChecklist
      x-api-path-slug: checklistsidchecklistname-put
      parameters:
      - in: body
        name: body
        description: Attributes of Checklists Name to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Name
  /checklists/{idChecklist}/pos:
    put:
      summary: Put Checklists Pos
      description: Put checklists pos.
      operationId: updateChecklistsPosByIdChecklist
      x-api-path-slug: checklistsidchecklistpos-put
      parameters:
      - in: body
        name: body
        description: Attributes of Checklists Pos to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Pos
  /checklists/{idChecklist}/{field}:
    get:
      summary: Get Checklists Field
      description: Get checklists field.
      operationId: getChecklistsByIdChecklistByField
      x-api-path-slug: checklistsidchecklistfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Field
  /labels:
    post:
      summary: Post Labels
      description: Post labels.
      operationId: addLabels
      x-api-path-slug: labels-post
      parameters:
      - in: body
        name: body
        description: Attributes of Labels to be added
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Labels
  /labels/{idLabel}:
    delete:
      summary: Delete Labels Label
      description: Delete labels label.
      operationId: deleteLabelsByIdLabel
      x-api-path-slug: labelsidlabel-delete
      parameters:
      - in: path
        name: idLabel
        description: idLabel
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Labels
      - Label
    get:
      summary: Get Labels Label
      description: Get labels label.
      operationId: getLabelsByIdLabel
      x-api-path-slug: labelsidlabel-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: color, idBoard, name or uses'
      - in: path
        name: idLabel
        description: idLabel
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Labels
      - Label
    put:
      summary: Put Labels Label
      description: Put labels label.
      operationId: updateLabelsByIdLabel
      x-api-path-slug: labelsidlabel-put
      parameters:
      - in: body
        name: body
        description: Attributes of Labels to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idLabel
        description: idLabel
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Labels
      - Label
  /labels/{idLabel}/board:
    get:
      summary: Get Labels Label Board
      description: Get labels label board.
      operationId: getLabelsBoardByIdLabel
      x-api-path-slug: labelsidlabelboard-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: closed, dateLastActivity,
          dateLastView, desc, descData, idOrganization, invitations, invited, labelNames,
          memberships, name, pinned, powerUps, prefs, shortLink, shortUrl, starred,
          subscribed or url'
      - in: path
        name: idLabel
        description: idLabel
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Labels
      - Label
      - Board
  /labels/{idLabel}/board/{field}:
    get:
      summary: Get Labels Label Board Field
      description: Get labels label board field.
      operationId: getLabelsBoardByIdLabelByField
      x-api-path-slug: labelsidlabelboardfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idLabel
        description: idLabel
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Labels
      - Label
      - Board
      - Field
  /labels/{idLabel}/color:
    put:
      summary: Put Labels Label Color
      description: Put labels label color.
      operationId: updateLabelsColorByIdLabel
      x-api-path-slug: labelsidlabelcolor-put
      parameters:
      - in: body
        name: body
        description: Attributes of Labels Color to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idLabel
        description: idLabel
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Labels
      - Label
      - Color
  /labels/{idLabel}/name:
    put:
      summary: Put Labels Label Name
      description: Put labels label name.
      operationId: updateLabelsNameByIdLabel
      x-api-path-slug: labelsidlabelname-put
      parameters:
      - in: body
        name: body
        description: Attributes of Labels Name to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idLabel
        description: idLabel
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Labels
      - Label
      - Name
  /lists:
    post:
      summary: Post Lists
      description: Post lists.
      operationId: addLists
      x-api-path-slug: lists-post
      parameters:
      - in: body
        name: body
        description: Attributes of Lists to be added
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Lists
  /lists/{idList}:
    get:
      summary: Get Lists List
      description: Get lists list.
      operationId: getListsByIdList
      x-api-path-slug: listsidlist-get
      parameters:
      - in: query
        name: board
        description: true or false
      - in: query
        name: board_fields
        description: 'all or a comma-separated list of: closed, dateLastActivity,
          dateLastView, desc, descData, idOrganization, invitations, invited, labelNames,
          memberships, name, pinned, powerUps, prefs, shortLink, shortUrl, starred,
          subscribed or url'
      - in: query
        name: cards
        description: 'One of: all, closed, none or open'
      - in: query
        name: card_fields
        description: 'all or a comma-separated list of: badges, checkItemStates, closed,
          dateLastActivity, desc, descData, due, email, idAttachmentCover, idBoard,
          idChecklists, idLabels, idList, idMembers, idMembersVoted, idShort, labels,
          manualCoverAttachment, name, pos, shortLink, shortUrl, subscribed or url'
      - in: query
        name: fields
        description: 'all or a comma-separated list of: closed, idBoard, name, pos
          or subscribed'
      - in: path
        name: idList
        description: idList
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Lists
      - List
    put:
      summary: Put Lists List
      description: Put lists list.
      operationId: updateListsByIdList
      x-api-path-slug: listsidlist-put
      parameters:
      - in: body
        name: body
        description: Attributes of Lists to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idList
        description: idList
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Lists
      - List
  /lists/{idList}/actions:
    get:
      summary: Get Lists List Actions
      description: Get lists list actions.
      operationId: getListsActionsByIdList
      x-api-path-slug: listsidlistactions-get
      parameters:
      - in: query
        name: before
        description: A date, or null
      - in: query
        name: display
        description: true or false
      - in: query
        name: entities
        description: true or false
      - in: query
        name: fields
        description: 'all or a comma-separated list of: data, date, idMemberCreator
          or type'
      - in: query
        name: filter
        description: 'all or a comma-separated list of: addAttachmentToCard, addChecklistToCard,
          addMemberToBoard, addMemberToCard, addMemberToOrganization, addToOrganizationBoard,
          commentCard, convertToCardFromCheckItem, copyBoard, copyCard, copyCommentCard,
          createBoard, createCard, createList, createOrganization, deleteAttachmentFromCard,
          deleteBoardInvitation, deleteCard, deleteOrganizationInvitation, disablePowerUp,
          emailCard, enablePowerUp, makeAdminOfBoard, makeNormalMemberOfBoard, makeNormalMemberOfOrganization,
          makeObserverOfBoard, memberJoinedTrello, moveCardFromBoard, moveCardToBoard,
          moveListFromBoard, moveListToBoard, removeChecklistFromCard, removeFromOrganizationBoard,
          removeMemberFromCard, unconfirmedBoardInvitation, unconfirmedOrganizationInvitation,
          updateBoard, updateCard, updateCard:closed, updateCard:desc, updateCard:idList,
          updateCard:name, updateCheckItemStateOnCard, updateChecklist, updateList,
          updateList:closed, updateList:name, updateMember or updateOrganization'
      - in: query
        name: format
        description: 'One of: count, list or minimal'
      - in: path
        name: idList
        description: idList
      - in: query
        name: idModels
        description: Only return actions related to these model ids
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: limit
        description: a number from 0 to 1000
      - in: query
        name: member
        description: true or false
      - in: query
        name: memberCreator
        description: true or false
      - in: query
        name: memberCreator_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: page
        description: Page * limit must be less than 1000
      - in: query
        name: since
        description: A date, null or lastView
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Lists
      - List
      - Actions
  /lists/{idList}/archiveAllCards:
    post:
      summary: Post Lists List Archiveallcards
      description: Post lists list archiveallcards.
      operationId: addListsArchiveAllCardsByIdList
      x-api-path-slug: listsidlistarchiveallcards-post
      parameters:
      - in: path
        name: idList
        description: idList
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Lists
      - List
      - Archiveallcards
  /lists/{idList}/board:
    get:
      summary: Get Lists List Board
      description: Get lists list board.
      operationId: getListsBoardByIdList
      x-api-path-slug: listsidlistboard-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: closed, dateLastActivity,
          dateLastView, desc, descData, idOrganization, invitations, invited, labelNames,
          memberships, name, pinned, powerUps, prefs, shortLink, shortUrl, starred,
          subscribed or url'
      - in: path
        name: idList
        description: idList
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Lists
      - List
      - Board
  /lists/{idList}/board/{field}:
    get:
      summary: Get Lists List Board Field
      description: Get lists list board field.
      operationId: getListsBoardByIdListByField
      x-api-path-slug: listsidlistboardfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idList
        description: idList
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Lists
      - List
      - Board
      - Field
  /lists/{idList}/cards:
    get:
      summary: Get Lists List Cards
      description: Get lists list cards.
      operationId: getListsCardsByIdList
      x-api-path-slug: listsidlistcards-get
      parameters:
      - in: query
        name: actions
        description: 'all or a comma-separated list of: addAttachmentToCard, addChecklistToCard,
          addMemberToBoard, addMemberToCard, addMemberToOrganization, addToOrganizationBoard,
          commentCard, convertToCardFromCheckItem, copyBoard, copyCard, copyCommentCard,
          createBoard, createCard, createList, createOrganization, deleteAttachmentFromCard,
          deleteBoardInvitation, deleteCard, deleteOrganizationInvitation, disablePowerUp,
          emailCard, enablePowerUp, makeAdminOfBoard, makeNormalMemberOfBoard, makeNormalMemberOfOrganization,
          makeObserverOfBoard, memberJoinedTrello, moveCardFromBoard, moveCardToBoard,
          moveListFromBoard, moveListToBoard, removeChecklistFromCard, removeFromOrganizationBoard,
          removeMemberFromCard, unconfirmedBoardInvitation, unconfirmedOrganizationInvitation,
          updateBoard, updateCard, updateCard:closed, updateCard:desc, updateCard:idList,
          updateCard:name, updateCheckItemStateOnCard, updateChecklist, updateList,
          updateList:closed, updateList:name, updateMember or updateOrganization'
      - in: query
        name: attachments
        description: A boolean value or &quot;cover&quot; for only card cover attachments
      - in: query
        name: attachment_fields
        description: 'all or a comma-separated list of: bytes, date, edgeColor, idMember,
          isUpload, mimeType, name, previews or url'
      - in: query
        name: before
        description: A date, or null
      - in: query
        name: checkItemStates
        description: true or false
      - in: query
        name: checklists
        description: 'One of: all or none'
      - in: query
        name: fields
        description: 'all or a comma-separated list of: badges, checkItemStates, closed,
          dateLastActivity, desc, descData, due, email, idAttachmentCover, idBoard,
          idChecklists, idLabels, idList, idMembers, idMembersVoted, idShort, labels,
          manualCoverAttachment, name, pos, shortLink, shortUrl, subscribed or url'
      - in: query
        name: filter
        description: 'One of: all, closed, none or open'
      - in: path
        name: idList
        description: idList
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: limit
        description: a number from 1 to 1000
      - in: query
        name: members
        description: true or false
      - in: query
        name: member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: since
        description: A date, or null
      - in: query
        name: stickers
        description: true or false
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Lists
      - List
      - Cards
    post:
      summary: Post Lists List Cards
      description: Post lists list cards.
      operationId: addListsCardsByIdList
      x-api-path-slug: listsidlistcards-post
      parameters:
      - in: body
        name: body
        description: Attributes of Lists Cards to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idList
        description: idList
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Lists
      - List
      - Cards
  /lists/{idList}/cards/{filter}:
    get:
      summary: Get Lists List Cards Filter
      description: Get lists list cards filter.
      operationId: getListsCardsByIdListByFilter
      x-api-path-slug: listsidlistcardsfilter-get
      parameters:
      - in: path
        name: filter
        description: filter
      - in: path
        name: idList
        description: idList
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Lists
      - List
      - Cards
      - Filter
  /lists/{idList}/closed:
    put:
      summary: Put Lists List Closed
      description: Put lists list closed.
      operationId: updateListsClosedByIdList
      x-api-path-slug: listsidlistclosed-put
      parameters:
      - in: body
        name: body
        description: Attributes of Lists Closed to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idList
        description: idList
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Lists
      - List
      - Closed
  /lists/{idList}/idBoard:
    put:
      summary: Put Lists List Board
      description: Put lists list board.
      operationId: updateListsIdBoardByIdList
      x-api-path-slug: listsidlistidboard-put
      parameters:
      - in: body
        name: body
        description: Attributes of Lists Id Board to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idList
        description: idList
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Lists
      - List
      - Board
  /lists/{idList}/moveAllCards:
    post:
      summary: Post Lists List Moveallcards
      description: Post lists list moveallcards.
      operationId: addListsMoveAllCardsByIdList
      x-api-path-slug: listsidlistmoveallcards-post
      parameters:
      - in: body
        name: body
        description: Attributes of Lists Move All Cards to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idList
        description: idList
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Lists
      - List
      - Moveallcards
  /lists/{idList}/name:
    put:
      summary: Put Lists List Name
      description: Put lists list name.
      operationId: updateListsNameByIdList
      x-api-path-slug: listsidlistname-put
      parameters:
      - in: body
        name: body
        description: Attributes of Lists Name to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idList
        description: idList
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Lists
      - List
      - Name
  /lists/{idList}/pos:
    put:
      summary: Put Lists List Pos
      description: Put lists list pos.
      operationId: updateListsPosByIdList
      x-api-path-slug: listsidlistpos-put
      parameters:
      - in: body
        name: body
        description: Attributes of Lists Pos to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idList
        description: idList
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Lists
      - List
      - Pos
  /lists/{idList}/subscribed:
    put:
      summary: Put Lists List Subscribed
      description: Put lists list subscribed.
      operationId: updateListsSubscribedByIdList
      x-api-path-slug: listsidlistsubscribed-put
      parameters:
      - in: body
        name: body
        description: Attributes of Lists Subscribed to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idList
        description: idList
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Lists
      - List
      - Subscribed
  /lists/{idList}/{field}:
    get:
      summary: Get Lists List Field
      description: Get lists list field.
      operationId: getListsByIdListByField
      x-api-path-slug: listsidlistfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idList
        description: idList
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Lists
      - List
      - Field
  /members/{idMember}:
    get:
      summary: Get Members
      description: Get members.
      operationId: getMembersByIdMember
      x-api-path-slug: membersidmember-get
      parameters:
      - in: query
        name: actions
        description: 'all or a comma-separated list of: addAttachmentToCard, addChecklistToCard,
          addMemberToBoard, addMemberToCard, addMemberToOrganization, addToOrganizationBoard,
          commentCard, convertToCardFromCheckItem, copyBoard, copyCard, copyCommentCard,
          createBoard, createCard, createList, createOrganization, deleteAttachmentFromCard,
          deleteBoardInvitation, deleteCard, deleteOrganizationInvitation, disablePowerUp,
          emailCard, enablePowerUp, makeAdminOfBoard, makeNormalMemberOfBoard, makeNormalMemberOfOrganization,
          makeObserverOfBoard, memberJoinedTrello, moveCardFromBoard, moveCardToBoard,
          moveListFromBoard, moveListToBoard, removeChecklistFromCard, removeFromOrganizationBoard,
          removeMemberFromCard, unconfirmedBoardInvitation, unconfirmedOrganizationInvitation,
          updateBoard, updateCard, updateCard:closed, updateCard:desc, updateCard:idList,
          updateCard:name, updateCheckItemStateOnCard, updateChecklist, updateList,
          updateList:closed, updateList:name, updateMember or updateOrganization'
      - in: query
        name: actions_display
        description: true or false
      - in: query
        name: actions_entities
        description: true or false
      - in: query
        name: actions_limit
        description: a number from 0 to 1000
      - in: query
        name: action_before
        description: A date, or null
      - in: query
        name: action_fields
        description: 'all or a comma-separated list of: data, date, idMemberCreator
          or type'
      - in: query
        name: action_since
        description: A date, null or lastView
      - in: query
        name: boardBackgrounds
        description: 'One of: all, custom, default, none or premium'
      - in: query
        name: boards
        description: 'all or a comma-separated list of: closed, members, open, organization,
          pinned, public, starred or unpinned'
      - in: query
        name: boardsInvited
        description: 'all or a comma-separated list of: closed, members, open, organization,
          pinned, public, starred or unpinned'
      - in: query
        name: boardsInvited_fields
        description: 'all or a comma-separated list of: closed, dateLastActivity,
          dateLastView, desc, descData, idOrganization, invitations, invited, labelNames,
          memberships, name, pinned, powerUps, prefs, shortLink, shortUrl, starred,
          subscribed or url'
      - in: query
        name: boardStars
        description: true or false
      - in: query
        name: board_actions
        description: 'all or a comma-separated list of: addAttachmentToCard, addChecklistToCard,
          addMemberToBoard, addMemberToCard, addMemberToOrganization, addToOrganizationBoard,
          commentCard, convertToCardFromCheckItem, copyBoard, copyCard, copyCommentCard,
          createBoard, createCard, createList, createOrganization, deleteAttachmentFromCard,
          deleteBoardInvitation, deleteCard, deleteOrganizationInvitation, disablePowerUp,
          emailCard, enablePowerUp, makeAdminOfBoard, makeNormalMemberOfBoard, makeNormalMemberOfOrganization,
          makeObserverOfBoard, memberJoinedTrello, moveCardFromBoard, moveCardToBoard,
          moveListFromBoard, moveListToBoard, removeChecklistFromCard, removeFromOrganizationBoard,
          removeMemberFromCard, unconfirmedBoardInvitation, unconfirmedOrganizationInvitation,
          updateBoard, updateCard, updateCard:closed, updateCard:desc, updateCard:idList,
          updateCard:name, updateCheckItemStateOnCard, updateChecklist, updateList,
          updateList:closed, updateList:name, updateMember or updateOrganization'
      - in: query
        name: board_actions_display
        description: true or false
      - in: query
        name: board_actions_entities
        description: true or false
      - in: query
        name: board_actions_format
        description: 'One of: count, list or minimal'
      - in: query
        name: board_actions_limit
        description: a number from 0 to 1000
      - in: query
        name: board_actions_since
        description: A date, null or lastView
      - in: query
        name: board_action_fields
        description: 'all or a comma-separated list of: data, date, idMemberCreator
          or type'
      - in: query
        name: board_fields
        description: 'all or a comma-separated list of: closed, dateLastActivity,
          dateLastView, desc, descData, idOrganization, invitations, invited, labelNames,
          memberships, name, pinned, powerUps, prefs, shortLink, shortUrl, starred,
          subscribed or url'
      - in: query
        name: board_lists
        description: 'One of: all, closed, none or open'
      - in: query
        name: board_memberships
        description: 'all or a comma-separated list of: active, admin, deactivated,
          me or normal'
      - in: query
        name: board_organization
        description: true or false
      - in: query
        name: board_organization_fields
        description: 'all or a comma-separated list of: billableMemberCount, desc,
          descData, displayName, idBoards, invitations, invited, logoHash, memberships,
          name, powerUps, prefs, premiumFeatures, products, url or website'
      - in: query
        name: cards
        description: 'One of: all, closed, none, open or visible'
      - in: query
        name: card_attachments
        description: A boolean value or &quot;cover&quot; for only card cover attachments
      - in: query
        name: card_attachment_fields
        description: 'all or a comma-separated list of: bytes, date, edgeColor, idMember,
          isUpload, mimeType, name, previews or url'
      - in: query
        name: card_fields
        description: 'all or a comma-separated list of: badges, checkItemStates, closed,
          dateLastActivity, desc, descData, due, email, idAttachmentCover, idBoard,
          idChecklists, idLabels, idList, idMembers, idMembersVoted, idShort, labels,
          manualCoverAttachment, name, pos, shortLink, shortUrl, subscribed or url'
      - in: query
        name: card_members
        description: true or false
      - in: query
        name: card_member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: card_stickers
        description: true or false
      - in: query
        name: customBoardBackgrounds
        description: 'One of: all or none'
      - in: query
        name: customEmoji
        description: 'One of: all or none'
      - in: query
        name: customStickers
        description: 'One of: all or none'
      - in: query
        name: fields
        description: 'all or a comma-separated list of: avatarHash, avatarSource,
          bio, bioData, confirmed, email, fullName, gravatarHash, idBoards, idBoardsPinned,
          idOrganizations, idPremOrgsAdmin, initials, loginTypes, memberType, oneTimeMessagesDismissed,
          prefs, premiumFeatures, products, status, status, trophies, uploadedAvatarHash,
          url or username'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: notifications
        description: 'all or a comma-separated list of: addAdminToBoard, addAdminToOrganization,
          addedAttachmentToCard, addedMemberToCard, addedToBoard, addedToCard, addedToOrganization,
          cardDueSoon, changeCard, closeBoard, commentCard, createdCard, declinedInvitationToBoard,
          declinedInvitationToOrganization, invitedToBoard, invitedToOrganization,
          makeAdminOfBoard, makeAdminOfOrganization, memberJoinedTrello, mentionedOnCard,
          removedFromBoard, removedFromCard, removedFromOrganization, removedMemberFromCard,
          unconfirmedInvitedToBoard, unconfirmedInvitedToOrganization or updateCheckItemStateOnCard'
      - in: query
        name: notifications_display
        description: true or false
      - in: query
        name: notifications_entities
        description: true or false
      - in: query
        name: notifications_limit
        description: a number from 1 to 1000
      - in: query
        name: notification_before
        description: An id, or null
      - in: query
        name: notification_fields
        description: 'all or a comma-separated list of: data, date, idMemberCreator,
          type or unread'
      - in: query
        name: notification_memberCreator
        description: true or false
      - in: query
        name: notification_memberCreator_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: notification_since
        description: An id, or null
      - in: query
        name: organizations
        description: 'One of: all, members, none or public'
      - in: query
        name: organizationsInvited
        description: 'One of: all, members, none or public'
      - in: query
        name: organizationsInvited_fields
        description: 'all or a comma-separated list of: billableMemberCount, desc,
          descData, displayName, idBoards, invitations, invited, logoHash, memberships,
          name, powerUps, prefs, premiumFeatures, products, url or website'
      - in: query
        name: organization_fields
        description: 'all or a comma-separated list of: billableMemberCount, desc,
          descData, displayName, idBoards, invitations, invited, logoHash, memberships,
          name, powerUps, prefs, premiumFeatures, products, url or website'
      - in: query
        name: organization_paid_account
        description: true or false
      - in: query
        name: paid_account
        description: true or false
      - in: query
        name: savedSearches
        description: true or false
      - in: query
        name: token
        description: Getting a token from a user
      - in: query
        name: tokens
        description: 'One of: all or none'
      responses:
        200:
          description: OK
      tags:
      - Members
    put:
      summary: Put Members
      description: Put members.
      operationId: updateMembersByIdMember
      x-api-path-slug: membersidmember-put
      parameters:
      - in: body
        name: body
        description: Attributes of Members to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
  /members/{idMember}/actions:
    get:
      summary: Get Members Actions
      description: Get members actions.
      operationId: getMembersActionsByIdMember
      x-api-path-slug: membersidmemberactions-get
      parameters:
      - in: query
        name: before
        description: A date, or null
      - in: query
        name: display
        description: true or false
      - in: query
        name: entities
        description: true or false
      - in: query
        name: fields
        description: 'all or a comma-separated list of: data, date, idMemberCreator
          or type'
      - in: query
        name: filter
        description: 'all or a comma-separated list of: addAttachmentToCard, addChecklistToCard,
          addMemberToBoard, addMemberToCard, addMemberToOrganization, addToOrganizationBoard,
          commentCard, convertToCardFromCheckItem, copyBoard, copyCard, copyCommentCard,
          createBoard, createCard, createList, createOrganization, deleteAttachmentFromCard,
          deleteBoardInvitation, deleteCard, deleteOrganizationInvitation, disablePowerUp,
          emailCard, enablePowerUp, makeAdminOfBoard, makeNormalMemberOfBoard, makeNormalMemberOfOrganization,
          makeObserverOfBoard, memberJoinedTrello, moveCardFromBoard, moveCardToBoard,
          moveListFromBoard, moveListToBoard, removeChecklistFromCard, removeFromOrganizationBoard,
          removeMemberFromCard, unconfirmedBoardInvitation, unconfirmedOrganizationInvitation,
          updateBoard, updateCard, updateCard:closed, updateCard:desc, updateCard:idList,
          updateCard:name, updateCheckItemStateOnCard, updateChecklist, updateList,
          updateList:closed, updateList:name, updateMember or updateOrganization'
      - in: query
        name: format
        description: 'One of: count, list or minimal'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: idModels
        description: Only return actions related to these model ids
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: limit
        description: a number from 0 to 1000
      - in: query
        name: member
        description: true or false
      - in: query
        name: memberCreator
        description: true or false
      - in: query
        name: memberCreator_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: page
        description: Page * limit must be less than 1000
      - in: query
        name: since
        description: A date, null or lastView
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Actions
  /members/{idMember}/avatar:
    post:
      summary: Post Members Avatar
      description: Post members avatar.
      operationId: addMembersAvatarByIdMember
      x-api-path-slug: membersidmemberavatar-post
      parameters:
      - in: body
        name: body
        description: Attributes of Members Avatar to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Avatar
  /members/{idMember}/avatarSource:
    put:
      summary: Put Members Avatarsource
      description: Put members avatarsource.
      operationId: updateMembersAvatarSourceByIdMember
      x-api-path-slug: membersidmemberavatarsource-put
      parameters:
      - in: body
        name: body
        description: Attributes of Members Avatar Source to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Avatarsource
  /members/{idMember}/bio:
    put:
      summary: Put Members Bio
      description: Put members bio.
      operationId: updateMembersBioByIdMember
      x-api-path-slug: membersidmemberbio-put
      parameters:
      - in: body
        name: body
        description: Attributes of Members Bio to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Bio
  /members/{idMember}/boardBackgrounds:
    get:
      summary: Get Members Boardbackgrounds
      description: Get members boardbackgrounds.
      operationId: getMembersBoardBackgroundsByIdMember
      x-api-path-slug: membersidmemberboardbackgrounds-get
      parameters:
      - in: query
        name: filter
        description: 'One of: all, custom, default, none or premium'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Boardbackgrounds
    post:
      summary: Post Members Boardbackgrounds
      description: Post members boardbackgrounds.
      operationId: addMembersBoardBackgroundsByIdMember
      x-api-path-slug: membersidmemberboardbackgrounds-post
      parameters:
      - in: body
        name: body
        description: Attributes of Members Board Backgrounds to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Boardbackgrounds
  /members/{idMember}/boardBackgrounds/{idBoardBackground}:
    delete:
      summary: Delete Members Boardbackgrounds Boardbackground
      description: Delete members boardbackgrounds boardbackground.
      operationId: deleteMembersBoardBackgroundsByIdMemberByIdBoardBackground
      x-api-path-slug: membersidmemberboardbackgroundsidboardbackground-delete
      parameters:
      - in: path
        name: idBoardBackground
        description: idBoardBackground
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Boardbackgrounds
      - Boardbackground
    get:
      summary: Get Members Boardbackgrounds Boardbackground
      description: Get members boardbackgrounds boardbackground.
      operationId: getMembersBoardBackgroundsByIdMemberByIdBoardBackground
      x-api-path-slug: membersidmemberboardbackgroundsidboardbackground-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: brightness, fullSizeUrl, scaled
          or tile'
      - in: path
        name: idBoardBackground
        description: idBoardBackground
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Boardbackgrounds
      - Boardbackground
    put:
      summary: Put Members Boardbackgrounds Boardbackground
      description: Put members boardbackgrounds boardbackground.
      operationId: updateMembersBoardBackgroundsByIdMemberByIdBoardBackground
      x-api-path-slug: membersidmemberboardbackgroundsidboardbackground-put
      parameters:
      - in: body
        name: body
        description: Attributes of Members Board Backgrounds to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoardBackground
        description: idBoardBackground
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Boardbackgrounds
      - Boardbackground
  /members/{idMember}/boardStars:
    get:
      summary: Get Members Boardstars
      description: Get members boardstars.
      operationId: getMembersBoardStarsByIdMember
      x-api-path-slug: membersidmemberboardstars-get
      parameters:
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Boardstars
    post:
      summary: Post Members Boardstars
      description: Post members boardstars.
      operationId: addMembersBoardStarsByIdMember
      x-api-path-slug: membersidmemberboardstars-post
      parameters:
      - in: body
        name: body
        description: Attributes of Members Board Stars to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Boardstars
  /members/{idMember}/boardStars/{idBoardStar}:
    delete:
      summary: Delete Members Boardstars
      description: Delete members boardstars.
      operationId: deleteMembersBoardStarsByIdMemberByIdBoardStar
      x-api-path-slug: membersidmemberboardstarsidboardstar-delete
      parameters:
      - in: path
        name: idBoardStar
        description: idBoardStar
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Boardstars
    get:
      summary: Get Members Boardstars
      description: Get members boardstars.
      operationId: getMembersBoardStarsByIdMemberByIdBoardStar
      x-api-path-slug: membersidmemberboardstarsidboardstar-get
      parameters:
      - in: path
        name: idBoardStar
        description: idBoardStar
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Boardstars
    put:
      summary: Put Members Boardstars
      description: Put members boardstars.
      operationId: updateMembersBoardStarsByIdMemberByIdBoardStar
      x-api-path-slug: membersidmemberboardstarsidboardstar-put
      parameters:
      - in: body
        name: body
        description: Attributes of Members Board Stars to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoardStar
        description: idBoardStar
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Boardstars
  /members/{idMember}/boardStars/{idBoardStar}/idBoard:
    put:
      summary: Put Members Boardstars Board
      description: Put members boardstars board.
      operationId: updateMembersBoardStarsIdBoardByIdMemberByIdBoardStar
      x-api-path-slug: membersidmemberboardstarsidboardstaridboard-put
      parameters:
      - in: body
        name: body
        description: Attributes of Members Board Stars Id Board to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoardStar
        description: idBoardStar
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Boardstars
      - Board
  /members/{idMember}/boardStars/{idBoardStar}/pos:
    put:
      summary: Put Members Boardstars Pos
      description: Put members boardstars pos.
      operationId: updateMembersBoardStarsPosByIdMemberByIdBoardStar
      x-api-path-slug: membersidmemberboardstarsidboardstarpos-put
      parameters:
      - in: body
        name: body
        description: Attributes of Members Board Stars Pos to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoardStar
        description: idBoardStar
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Boardstars
      - Pos
  /members/{idMember}/boards:
    get:
      summary: Get Members Boards
      description: Get members boards.
      operationId: getMembersBoardsByIdMember
      x-api-path-slug: membersidmemberboards-get
      parameters:
      - in: query
        name: actions
        description: 'all or a comma-separated list of: addAttachmentToCard, addChecklistToCard,
          addMemberToBoard, addMemberToCard, addMemberToOrganization, addToOrganizationBoard,
          commentCard, convertToCardFromCheckItem, copyBoard, copyCard, copyCommentCard,
          createBoard, createCard, createList, createOrganization, deleteAttachmentFromCard,
          deleteBoardInvitation, deleteCard, deleteOrganizationInvitation, disablePowerUp,
          emailCard, enablePowerUp, makeAdminOfBoard, makeNormalMemberOfBoard, makeNormalMemberOfOrganization,
          makeObserverOfBoard, memberJoinedTrello, moveCardFromBoard, moveCardToBoard,
          moveListFromBoard, moveListToBoard, removeChecklistFromCard, removeFromOrganizationBoard,
          removeMemberFromCard, unconfirmedBoardInvitation, unconfirmedOrganizationInvitation,
          updateBoard, updateCard, updateCard:closed, updateCard:desc, updateCard:idList,
          updateCard:name, updateCheckItemStateOnCard, updateChecklist, updateList,
          updateList:closed, updateList:name, updateMember or updateOrganization'
      - in: query
        name: actions_entities
        description: true or false
      - in: query
        name: actions_format
        description: 'One of: count, list or minimal'
      - in: query
        name: actions_limit
        description: a number from 0 to 1000
      - in: query
        name: actions_since
        description: A date, null or lastView
      - in: query
        name: action_fields
        description: 'all or a comma-separated list of: data, date, idMemberCreator
          or type'
      - in: query
        name: fields
        description: 'all or a comma-separated list of: closed, dateLastActivity,
          dateLastView, desc, descData, idOrganization, invitations, invited, labelNames,
          memberships, name, pinned, powerUps, prefs, shortLink, shortUrl, starred,
          subscribed or url'
      - in: query
        name: filter
        description: 'all or a comma-separated list of: closed, members, open, organization,
          pinned, public, starred or unpinned'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: lists
        description: 'One of: all, closed, none or open'
      - in: query
        name: memberships
        description: 'all or a comma-separated list of: active, admin, deactivated,
          me or normal'
      - in: query
        name: organization
        description: true or false
      - in: query
        name: organization_fields
        description: 'all or a comma-separated list of: billableMemberCount, desc,
          descData, displayName, idBoards, invitations, invited, logoHash, memberships,
          name, powerUps, prefs, premiumFeatures, products, url or website'
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Boards
  /members/{idMember}/boards/{filter}:
    get:
      summary: Get Members Boards Filter
      description: Get members boards filter.
      operationId: getMembersBoardsByIdMemberByFilter
      x-api-path-slug: membersidmemberboardsfilter-get
      parameters:
      - in: path
        name: filter
        description: filter
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Boards
      - Filter
  /members/{idMember}/boardsInvited:
    get:
      summary: Get Members Boardsinvited
      description: Get members boardsinvited.
      operationId: getMembersBoardsInvitedByIdMember
      x-api-path-slug: membersidmemberboardsinvited-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: closed, dateLastActivity,
          dateLastView, desc, descData, idOrganization, invitations, invited, labelNames,
          memberships, name, pinned, powerUps, prefs, shortLink, shortUrl, starred,
          subscribed or url'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Boardsinvited
  /members/{idMember}/boardsInvited/{field}:
    get:
      summary: Get Members Boardsinvited Field
      description: Get members boardsinvited field.
      operationId: getMembersBoardsInvitedByIdMemberByField
      x-api-path-slug: membersidmemberboardsinvitedfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Boardsinvited
      - Field
  /members/{idMember}/cards:
    get:
      summary: Get Members Cards
      description: Get members cards.
      operationId: getMembersCardsByIdMember
      x-api-path-slug: membersidmembercards-get
      parameters:
      - in: query
        name: actions
        description: 'all or a comma-separated list of: addAttachmentToCard, addChecklistToCard,
          addMemberToBoard, addMemberToCard, addMemberToOrganization, addToOrganizationBoard,
          commentCard, convertToCardFromCheckItem, copyBoard, copyCard, copyCommentCard,
          createBoard, createCard, createList, createOrganization, deleteAttachmentFromCard,
          deleteBoardInvitation, deleteCard, deleteOrganizationInvitation, disablePowerUp,
          emailCard, enablePowerUp, makeAdminOfBoard, makeNormalMemberOfBoard, makeNormalMemberOfOrganization,
          makeObserverOfBoard, memberJoinedTrello, moveCardFromBoard, moveCardToBoard,
          moveListFromBoard, moveListToBoard, removeChecklistFromCard, removeFromOrganizationBoard,
          removeMemberFromCard, unconfirmedBoardInvitation, unconfirmedOrganizationInvitation,
          updateBoard, updateCard, updateCard:closed, updateCard:desc, updateCard:idList,
          updateCard:name, updateCheckItemStateOnCard, updateChecklist, updateList,
          updateList:closed, updateList:name, updateMember or updateOrganization'
      - in: query
        name: attachments
        description: A boolean value or &quot;cover&quot; for only card cover attachments
      - in: query
        name: attachment_fields
        description: 'all or a comma-separated list of: bytes, date, edgeColor, idMember,
          isUpload, mimeType, name, previews or url'
      - in: query
        name: before
        description: A date, or null
      - in: query
        name: checkItemStates
        description: true or false
      - in: query
        name: checklists
        description: 'One of: all or none'
      - in: query
        name: fields
        description: 'all or a comma-separated list of: badges, checkItemStates, closed,
          dateLastActivity, desc, descData, due, email, idAttachmentCover, idBoard,
          idChecklists, idLabels, idList, idMembers, idMembersVoted, idShort, labels,
          manualCoverAttachment, name, pos, shortLink, shortUrl, subscribed or url'
      - in: query
        name: filter
        description: 'One of: all, closed, none, open or visible'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: limit
        description: a number from 1 to 1000
      - in: query
        name: members
        description: true or false
      - in: query
        name: member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: since
        description: A date, or null
      - in: query
        name: stickers
        description: true or false
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Cards
  /members/{idMember}/cards/{filter}:
    get:
      summary: Get Members Cards Filter
      description: Get members cards filter.
      operationId: getMembersCardsByIdMemberByFilter
      x-api-path-slug: membersidmembercardsfilter-get
      parameters:
      - in: path
        name: filter
        description: filter
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Cards
      - Filter
  /members/{idMember}/customBoardBackgrounds:
    get:
      summary: Get Members Customboardbackgrounds
      description: Get members customboardbackgrounds.
      operationId: getMembersCustomBoardBackgroundsByIdMember
      x-api-path-slug: membersidmembercustomboardbackgrounds-get
      parameters:
      - in: query
        name: filter
        description: 'One of: all or none'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Customboardbackgrounds
    post:
      summary: Post Members Customboardbackgrounds
      description: Post members customboardbackgrounds.
      operationId: addMembersCustomBoardBackgroundsByIdMember
      x-api-path-slug: membersidmembercustomboardbackgrounds-post
      parameters:
      - in: body
        name: body
        description: Attributes of Members Custom Board Backgrounds to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Customboardbackgrounds
  /members/{idMember}/customBoardBackgrounds/{idBoardBackground}:
    delete:
      summary: Delete Members Customboardbackgrounds Boardbackground
      description: Delete members customboardbackgrounds boardbackground.
      operationId: deleteMembersCustomBoardBackgroundsByIdMemberByIdBoardBackground
      x-api-path-slug: membersidmembercustomboardbackgroundsidboardbackground-delete
      parameters:
      - in: path
        name: idBoardBackground
        description: idBoardBackground
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Customboardbackgrounds
      - Boardbackground
    get:
      summary: Get Members Customboardbackgrounds Boardbackground
      description: Get members customboardbackgrounds boardbackground.
      operationId: getMembersCustomBoardBackgroundsByIdMemberByIdBoardBackground
      x-api-path-slug: membersidmembercustomboardbackgroundsidboardbackground-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: brightness, fullSizeUrl, scaled
          or tile'
      - in: path
        name: idBoardBackground
        description: idBoardBackground
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Customboardbackgrounds
      - Boardbackground
    put:
      summary: Put Members Customboardbackgrounds Boardbackground
      description: Put members customboardbackgrounds boardbackground.
      operationId: updateMembersCustomBoardBackgroundsByIdMemberByIdBoardBackground
      x-api-path-slug: membersidmembercustomboardbackgroundsidboardbackground-put
      parameters:
      - in: body
        name: body
        description: Attributes of Members Custom Board Backgrounds to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoardBackground
        description: idBoardBackground
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Customboardbackgrounds
      - Boardbackground
  /members/{idMember}/customEmoji:
    get:
      summary: Get Members Customemoji
      description: Get members customemoji.
      operationId: getMembersCustomEmojiByIdMember
      x-api-path-slug: membersidmembercustomemoji-get
      parameters:
      - in: query
        name: filter
        description: 'One of: all or none'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Customemoji
    post:
      summary: Post Members Customemoji
      description: Post members customemoji.
      operationId: addMembersCustomEmojiByIdMember
      x-api-path-slug: membersidmembercustomemoji-post
      parameters:
      - in: body
        name: body
        description: Attributes of Members Custom Emoji to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Customemoji
  /members/{idMember}/customEmoji/{idCustomEmoji}:
    get:
      summary: Get Members Customemoji Customemoji
      description: Get members customemoji customemoji.
      operationId: getMembersCustomEmojiByIdMemberByIdCustomEmoji
      x-api-path-slug: membersidmembercustomemojiidcustomemoji-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: name or url'
      - in: path
        name: idCustomEmoji
        description: idCustomEmoji
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Customemoji
      - Customemoji
  /members/{idMember}/customStickers:
    get:
      summary: Get Members Customstickers
      description: Get members customstickers.
      operationId: getMembersCustomStickersByIdMember
      x-api-path-slug: membersidmembercustomstickers-get
      parameters:
      - in: query
        name: filter
        description: 'One of: all or none'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Customstickers
    post:
      summary: Post Members Customstickers
      description: Post members customstickers.
      operationId: addMembersCustomStickersByIdMember
      x-api-path-slug: membersidmembercustomstickers-post
      parameters:
      - in: body
        name: body
        description: Attributes of Members Custom Stickers to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Customstickers
  /members/{idMember}/customStickers/{idCustomSticker}:
    delete:
      summary: Delete Members Customstickers Customsticker
      description: Delete members customstickers customsticker.
      operationId: deleteMembersCustomStickersByIdMemberByIdCustomSticker
      x-api-path-slug: membersidmembercustomstickersidcustomsticker-delete
      parameters:
      - in: path
        name: idCustomSticker
        description: idCustomSticker
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Customstickers
      - Customsticker
    get:
      summary: Get Members Customstickers Customsticker
      description: Get members customstickers customsticker.
      operationId: getMembersCustomStickersByIdMemberByIdCustomSticker
      x-api-path-slug: membersidmembercustomstickersidcustomsticker-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: scaled or url'
      - in: path
        name: idCustomSticker
        description: idCustomSticker
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Customstickers
      - Customsticker
  /members/{idMember}/deltas:
    get:
      summary: Get Members Deltas
      description: Get members deltas.
      operationId: getMembersDeltasByIdMember
      x-api-path-slug: membersidmemberdeltas-get
      parameters:
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: ixLastUpdate
        description: a number from -1 to Infinity
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: tags
        description: A valid tag for subscribing
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Deltas
  /members/{idMember}/fullName:
    put:
      summary: Put Members Fullname
      description: Put members fullname.
      operationId: updateMembersFullNameByIdMember
      x-api-path-slug: membersidmemberfullname-put
      parameters:
      - in: body
        name: body
        description: Attributes of Members Full Name to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Fullname
  /members/{idMember}/initials:
    put:
      summary: Put Members Initials
      description: Put members initials.
      operationId: updateMembersInitialsByIdMember
      x-api-path-slug: membersidmemberinitials-put
      parameters:
      - in: body
        name: body
        description: Attributes of Members Initials to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Initials
  /members/{idMember}/notifications:
    get:
      summary: Get Members Notifications
      description: Get members notifications.
      operationId: getMembersNotificationsByIdMember
      x-api-path-slug: membersidmembernotifications-get
      parameters:
      - in: query
        name: before
        description: An id, or null
      - in: query
        name: display
        description: true or false
      - in: query
        name: entities
        description: true or false
      - in: query
        name: fields
        description: 'all or a comma-separated list of: data, date, idMemberCreator,
          type or unread'
      - in: query
        name: filter
        description: 'all or a comma-separated list of: addAdminToBoard, addAdminToOrganization,
          addedAttachmentToCard, addedMemberToCard, addedToBoard, addedToCard, addedToOrganization,
          cardDueSoon, changeCard, closeBoard, commentCard, createdCard, declinedInvitationToBoard,
          declinedInvitationToOrganization, invitedToBoard, invitedToOrganization,
          makeAdminOfBoard, makeAdminOfOrganization, memberJoinedTrello, mentionedOnCard,
          removedFromBoard, removedFromCard, removedFromOrganization, removedMemberFromCard,
          unconfirmedInvitedToBoard, unconfirmedInvitedToOrganization or updateCheckItemStateOnCard'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: limit
        description: a number from 1 to 1000
      - in: query
        name: memberCreator
        description: true or false
      - in: query
        name: memberCreator_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: page
        description: a number from 0 to 100
      - in: query
        name: read_filter
        description: 'One of: all, read or unread'
      - in: query
        name: since
        description: An id, or null
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Notifications
  /members/{idMember}/notifications/{filter}:
    get:
      summary: Get Members Notifications Filter
      description: Get members notifications filter.
      operationId: getMembersNotificationsByIdMemberByFilter
      x-api-path-slug: membersidmembernotificationsfilter-get
      parameters:
      - in: path
        name: filter
        description: filter
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Notifications
      - Filter
  /members/{idMember}/oneTimeMessagesDismissed:
    post:
      summary: Post Members Onetimemessagesdismissed
      description: Post members onetimemessagesdismissed.
      operationId: addMembersOneTimeMessagesDismissedByIdMember
      x-api-path-slug: membersidmemberonetimemessagesdismissed-post
      parameters:
      - in: body
        name: body
        description: Attributes of Members One Time Messages Dismissed to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Onetimemessagesdismissed
  /members/{idMember}/organizations:
    get:
      summary: Get Members Organizations
      description: Get members organizations.
      operationId: getMembersOrganizationsByIdMember
      x-api-path-slug: membersidmemberorganizations-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: billableMemberCount, desc,
          descData, displayName, idBoards, invitations, invited, logoHash, memberships,
          name, powerUps, prefs, premiumFeatures, products, url or website'
      - in: query
        name: filter
        description: 'One of: all, members, none or public'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: paid_account
        description: true or false
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Organizations
  /members/{idMember}/organizations/{filter}:
    get:
      summary: Get Members Organizations Filter
      description: Get members organizations filter.
      operationId: getMembersOrganizationsByIdMemberByFilter
      x-api-path-slug: membersidmemberorganizationsfilter-get
      parameters:
      - in: path
        name: filter
        description: filter
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Organizations
      - Filter
  /members/{idMember}/organizationsInvited:
    get:
      summary: Get Members Organizationsinvited
      description: Get members organizationsinvited.
      operationId: getMembersOrganizationsInvitedByIdMember
      x-api-path-slug: membersidmemberorganizationsinvited-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: billableMemberCount, desc,
          descData, displayName, idBoards, invitations, invited, logoHash, memberships,
          name, powerUps, prefs, premiumFeatures, products, url or website'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Organizationsinvited
  /members/{idMember}/organizationsInvited/{field}:
    get:
      summary: Get Members Organizationsinvited Field
      description: Get members organizationsinvited field.
      operationId: getMembersOrganizationsInvitedByIdMemberByField
      x-api-path-slug: membersidmemberorganizationsinvitedfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Organizationsinvited
      - Field
  /members/{idMember}/prefs/colorBlind:
    put:
      summary: Put Members Preferences Colorblind
      description: Put members preferences colorblind.
      operationId: updateMembersPrefsColorBlindByIdMember
      x-api-path-slug: membersidmemberprefscolorblind-put
      parameters:
      - in: body
        name: body
        description: Attributes of Prefs Color Blind to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Preferences
      - Colorblind
  /members/{idMember}/prefs/locale:
    put:
      summary: Put Members Preferences Locale
      description: Put members preferences locale.
      operationId: updateMembersPrefsLocaleByIdMember
      x-api-path-slug: membersidmemberprefslocale-put
      parameters:
      - in: body
        name: body
        description: Attributes of Prefs Locale to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Preferences
      - Locale
  /members/{idMember}/prefs/minutesBetweenSummaries:
    put:
      summary: Put Members Preferences Minutesbetweensummaries
      description: Put members preferences minutesbetweensummaries.
      operationId: updateMembersPrefsMinutesBetweenSummariesByIdMember
      x-api-path-slug: membersidmemberprefsminutesbetweensummaries-put
      parameters:
      - in: body
        name: body
        description: Attributes of Prefs Minutes Between Summaries to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Preferences
      - Minutesbetweensummaries
  /members/{idMember}/savedSearches:
    get:
      summary: Get Members Savedsearches
      description: Get members savedsearches.
      operationId: getMembersSavedSearchesByIdMember
      x-api-path-slug: membersidmembersavedsearches-get
      parameters:
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Savedsearches
    post:
      summary: Post Members Savedsearches
      description: Post members savedsearches.
      operationId: addMembersSavedSearchesByIdMember
      x-api-path-slug: membersidmembersavedsearches-post
      parameters:
      - in: body
        name: body
        description: Attributes of Members Saved Searches to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Savedsearches
  /members/{idMember}/savedSearches/{idSavedSearch}:
    delete:
      summary: Delete Members Savedsearches Savedsearch
      description: Delete members savedsearches savedsearch.
      operationId: deleteMembersSavedSearchesByIdMemberByIdSavedSearch
      x-api-path-slug: membersidmembersavedsearchesidsavedsearch-delete
      parameters:
      - in: path
        name: idMember
        description: idMember or username
      - in: path
        name: idSavedSearch
        description: idSavedSearch
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Savedsearches
      - Savedsearch
    get:
      summary: Get Members Savedsearches Savedsearch
      description: Get members savedsearches savedsearch.
      operationId: getMembersSavedSearchesByIdMemberByIdSavedSearch
      x-api-path-slug: membersidmembersavedsearchesidsavedsearch-get
      parameters:
      - in: path
        name: idMember
        description: idMember or username
      - in: path
        name: idSavedSearch
        description: idSavedSearch
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Savedsearches
      - Savedsearch
    put:
      summary: Put Members Savedsearches Savedsearch
      description: Put members savedsearches savedsearch.
      operationId: updateMembersSavedSearchesByIdMemberByIdSavedSearch
      x-api-path-slug: membersidmembersavedsearchesidsavedsearch-put
      parameters:
      - in: body
        name: body
        description: Attributes of Members Saved Searches to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember or username
      - in: path
        name: idSavedSearch
        description: idSavedSearch
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Savedsearches
      - Savedsearch
  /members/{idMember}/savedSearches/{idSavedSearch}/name:
    put:
      summary: Put Members Savedsearches Savedsearch Name
      description: Put members savedsearches savedsearch name.
      operationId: updateMembersSavedSearchesNameByIdMemberByIdSavedSearch
      x-api-path-slug: membersidmembersavedsearchesidsavedsearchname-put
      parameters:
      - in: body
        name: body
        description: Attributes of Members Saved Searches Name to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember or username
      - in: path
        name: idSavedSearch
        description: idSavedSearch
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Savedsearches
      - Savedsearch
      - Name
  /members/{idMember}/savedSearches/{idSavedSearch}/pos:
    put:
      summary: Put Members Savedsearches Savedsearch Pos
      description: Put members savedsearches savedsearch pos.
      operationId: updateMembersSavedSearchesPosByIdMemberByIdSavedSearch
      x-api-path-slug: membersidmembersavedsearchesidsavedsearchpos-put
      parameters:
      - in: body
        name: body
        description: Attributes of Members Saved Searches Pos to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember or username
      - in: path
        name: idSavedSearch
        description: idSavedSearch
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Savedsearches
      - Savedsearch
      - Pos
  /members/{idMember}/savedSearches/{idSavedSearch}/query:
    put:
      summary: Put Members Savedsearches Savedsearch Query
      description: Put members savedsearches savedsearch query.
      operationId: updateMembersSavedSearchesQueryByIdMemberByIdSavedSearch
      x-api-path-slug: membersidmembersavedsearchesidsavedsearchquery-put
      parameters:
      - in: body
        name: body
        description: Attributes of Members Saved Searches Query to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember or username
      - in: path
        name: idSavedSearch
        description: idSavedSearch
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Savedsearches
      - Savedsearch
      - Query
  /members/{idMember}/tokens:
    get:
      summary: Get Members Tokens
      description: Get members tokens.
      operationId: getMembersTokensByIdMember
      x-api-path-slug: membersidmembertokens-get
      parameters:
      - in: query
        name: filter
        description: 'One of: all or none'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Tokens
  /members/{idMember}/username:
    put:
      summary: Put Members Username
      description: Put members username.
      operationId: updateMembersUsernameByIdMember
      x-api-path-slug: membersidmemberusername-put
      parameters:
      - in: body
        name: body
        description: Attributes of Members Username to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Username
  /members/{idMember}/{field}:
    get:
      summary: Get Members Field
      description: Get members field.
      operationId: getMembersByIdMemberByField
      x-api-path-slug: membersidmemberfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idMember
        description: idMember or username
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Field
  /notifications/all/read:
    post:
      summary: Post Notifications All Read
      description: Post notifications all read.
      operationId: addNotificationsAllRead
      x-api-path-slug: notificationsallread-post
      parameters:
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Notifications
      - ""
      - Read
  /notifications/{idNotification}:
    get:
      summary: Get Notifications Notification
      description: Get notifications notification.
      operationId: getNotificationsByIdNotification
      x-api-path-slug: notificationsidnotification-get
      parameters:
      - in: query
        name: board
        description: true or false
      - in: query
        name: board_fields
        description: 'all or a comma-separated list of: closed, dateLastActivity,
          dateLastView, desc, descData, idOrganization, invitations, invited, labelNames,
          memberships, name, pinned, powerUps, prefs, shortLink, shortUrl, starred,
          subscribed or url'
      - in: query
        name: card
        description: true or false
      - in: query
        name: card_fields
        description: 'all or a comma-separated list of: badges, checkItemStates, closed,
          dateLastActivity, desc, descData, due, email, idAttachmentCover, idBoard,
          idChecklists, idLabels, idList, idMembers, idMembersVoted, idShort, labels,
          manualCoverAttachment, name, pos, shortLink, shortUrl, subscribed or url'
      - in: query
        name: display
        description: true or false
      - in: query
        name: entities
        description: true or false
      - in: query
        name: fields
        description: 'all or a comma-separated list of: data, date, idMemberCreator,
          type or unread'
      - in: path
        name: idNotification
        description: idNotification
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: list
        description: true or false
      - in: query
        name: member
        description: true or false
      - in: query
        name: memberCreator
        description: true or false
      - in: query
        name: memberCreator_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: organization
        description: true or false
      - in: query
        name: organization_fields
        description: 'all or a comma-separated list of: billableMemberCount, desc,
          descData, displayName, idBoards, invitations, invited, logoHash, memberships,
          name, powerUps, prefs, premiumFeatures, products, url or website'
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Notifications
      - Notification
    put:
      summary: Put Notifications Notification
      description: Put notifications notification.
      operationId: updateNotificationsByIdNotification
      x-api-path-slug: notificationsidnotification-put
      parameters:
      - in: body
        name: body
        description: Attributes of Notifications to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idNotification
        description: idNotification
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Notifications
      - Notification
  /notifications/{idNotification}/board:
    get:
      summary: Get Notifications Notification Board
      description: Get notifications notification board.
      operationId: getNotificationsBoardByIdNotification
      x-api-path-slug: notificationsidnotificationboard-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: closed, dateLastActivity,
          dateLastView, desc, descData, idOrganization, invitations, invited, labelNames,
          memberships, name, pinned, powerUps, prefs, shortLink, shortUrl, starred,
          subscribed or url'
      - in: path
        name: idNotification
        description: idNotification
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Notifications
      - Notification
      - Board
  /notifications/{idNotification}/board/{field}:
    get:
      summary: Get Notifications Notification Board Field
      description: Get notifications notification board field.
      operationId: getNotificationsBoardByIdNotificationByField
      x-api-path-slug: notificationsidnotificationboardfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idNotification
        description: idNotification
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Notifications
      - Notification
      - Board
      - Field
  /notifications/{idNotification}/card:
    get:
      summary: Get Notifications Notification Card
      description: Get notifications notification card.
      operationId: getNotificationsCardByIdNotification
      x-api-path-slug: notificationsidnotificationcard-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: badges, checkItemStates, closed,
          dateLastActivity, desc, descData, due, email, idAttachmentCover, idBoard,
          idChecklists, idLabels, idList, idMembers, idMembersVoted, idShort, labels,
          manualCoverAttachment, name, pos, shortLink, shortUrl, subscribed or url'
      - in: path
        name: idNotification
        description: idNotification
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Notifications
      - Notification
      - Card
  /notifications/{idNotification}/card/{field}:
    get:
      summary: Get Notifications Notification Card Field
      description: Get notifications notification card field.
      operationId: getNotificationsCardByIdNotificationByField
      x-api-path-slug: notificationsidnotificationcardfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idNotification
        description: idNotification
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Notifications
      - Notification
      - Card
      - Field
  /notifications/{idNotification}/display:
    get:
      summary: Get Notifications Notification Display
      description: Get notifications notification display.
      operationId: getNotificationsDisplayByIdNotification
      x-api-path-slug: notificationsidnotificationdisplay-get
      parameters:
      - in: path
        name: idNotification
        description: idNotification
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Notifications
      - Notification
      - Display
  /notifications/{idNotification}/entities:
    get:
      summary: Get Notifications Notification Entities
      description: Get notifications notification entities.
      operationId: getNotificationsEntitiesByIdNotification
      x-api-path-slug: notificationsidnotificationentities-get
      parameters:
      - in: path
        name: idNotification
        description: idNotification
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Notifications
      - Notification
      - Entities
  /notifications/{idNotification}/list:
    get:
      summary: Get Notifications Notification List
      description: Get notifications notification list.
      operationId: getNotificationsListByIdNotification
      x-api-path-slug: notificationsidnotificationlist-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: closed, idBoard, name, pos
          or subscribed'
      - in: path
        name: idNotification
        description: idNotification
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Notifications
      - Notification
      - List
  /notifications/{idNotification}/list/{field}:
    get:
      summary: Get Notifications Notification List Field
      description: Get notifications notification list field.
      operationId: getNotificationsListByIdNotificationByField
      x-api-path-slug: notificationsidnotificationlistfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idNotification
        description: idNotification
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Notifications
      - Notification
      - List
      - Field
  /notifications/{idNotification}/member:
    get:
      summary: Get Notifications Notification Member
      description: Get notifications notification member.
      operationId: getNotificationsMemberByIdNotification
      x-api-path-slug: notificationsidnotificationmember-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: avatarHash, avatarSource,
          bio, bioData, confirmed, email, fullName, gravatarHash, idBoards, idBoardsPinned,
          idOrganizations, idPremOrgsAdmin, initials, loginTypes, memberType, oneTimeMessagesDismissed,
          prefs, premiumFeatures, products, status, status, trophies, uploadedAvatarHash,
          url or username'
      - in: path
        name: idNotification
        description: idNotification
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Notifications
      - Notification
      - Member
  /notifications/{idNotification}/member/{field}:
    get:
      summary: Get Notifications Notification Member Field
      description: Get notifications notification member field.
      operationId: getNotificationsMemberByIdNotificationByField
      x-api-path-slug: notificationsidnotificationmemberfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idNotification
        description: idNotification
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Notifications
      - Notification
      - Member
      - Field
  /notifications/{idNotification}/memberCreator:
    get:
      summary: Get Notifications Notification Member Creator
      description: Get notifications notification member creator.
      operationId: getNotificationsMemberCreatorByIdNotification
      x-api-path-slug: notificationsidnotificationmembercreator-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: avatarHash, avatarSource,
          bio, bioData, confirmed, email, fullName, gravatarHash, idBoards, idBoardsPinned,
          idOrganizations, idPremOrgsAdmin, initials, loginTypes, memberType, oneTimeMessagesDismissed,
          prefs, premiumFeatures, products, status, status, trophies, uploadedAvatarHash,
          url or username'
      - in: path
        name: idNotification
        description: idNotification
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Notifications
      - Notification
      - Member
      - Creator
  /notifications/{idNotification}/memberCreator/{field}:
    get:
      summary: Get Notifications Notification Member Creator Field
      description: Get notifications notification member creator field.
      operationId: getNotificationsMemberCreatorByIdNotificationByField
      x-api-path-slug: notificationsidnotificationmembercreatorfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idNotification
        description: idNotification
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Notifications
      - Notification
      - Member
      - Creator
      - Field
  /notifications/{idNotification}/organization:
    get:
      summary: Get Notifications Notification Organization
      description: Get notifications notification organization.
      operationId: getNotificationsOrganizationByIdNotification
      x-api-path-slug: notificationsidnotificationorganization-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: billableMemberCount, desc,
          descData, displayName, idBoards, invitations, invited, logoHash, memberships,
          name, powerUps, prefs, premiumFeatures, products, url or website'
      - in: path
        name: idNotification
        description: idNotification
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Notifications
      - Notification
      - Organization
  /notifications/{idNotification}/organization/{field}:
    get:
      summary: Get Notifications Notification Organization Field
      description: Get notifications notification organization field.
      operationId: getNotificationsOrganizationByIdNotificationByField
      x-api-path-slug: notificationsidnotificationorganizationfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idNotification
        description: idNotification
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Notifications
      - Notification
      - Organization
      - Field
  /notifications/{idNotification}/unread:
    put:
      summary: Put Notifications Notification Unread
      description: Put notifications notification unread.
      operationId: updateNotificationsUnreadByIdNotification
      x-api-path-slug: notificationsidnotificationunread-put
      parameters:
      - in: body
        name: body
        description: Attributes of Notifications Unread to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idNotification
        description: idNotification
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Notifications
      - Notification
      - Unread
  /notifications/{idNotification}/{field}:
    get:
      summary: Get Notifications Notification Field
      description: Get notifications notification field.
      operationId: getNotificationsByIdNotificationByField
      x-api-path-slug: notificationsidnotificationfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idNotification
        description: idNotification
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Notifications
      - Notification
      - Field
  /organizations:
    post:
      summary: Post Organizations
      description: Post organizations.
      operationId: addOrganizations
      x-api-path-slug: organizations-post
      parameters:
      - in: body
        name: body
        description: Attributes of Organizations to be added
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
  /organizations/{idOrg}:
    delete:
      summary: Delete Organizations
      description: Delete organizations.
      operationId: deleteOrganizationsByIdOrg
      x-api-path-slug: organizationsidorg-delete
      parameters:
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
    get:
      summary: Get Organizations
      description: Get organizations.
      operationId: getOrganizationsByIdOrg
      x-api-path-slug: organizationsidorg-get
      parameters:
      - in: query
        name: actions
        description: 'all or a comma-separated list of: addAttachmentToCard, addChecklistToCard,
          addMemberToBoard, addMemberToCard, addMemberToOrganization, addToOrganizationBoard,
          commentCard, convertToCardFromCheckItem, copyBoard, copyCard, copyCommentCard,
          createBoard, createCard, createList, createOrganization, deleteAttachmentFromCard,
          deleteBoardInvitation, deleteCard, deleteOrganizationInvitation, disablePowerUp,
          emailCard, enablePowerUp, makeAdminOfBoard, makeNormalMemberOfBoard, makeNormalMemberOfOrganization,
          makeObserverOfBoard, memberJoinedTrello, moveCardFromBoard, moveCardToBoard,
          moveListFromBoard, moveListToBoard, removeChecklistFromCard, removeFromOrganizationBoard,
          removeMemberFromCard, unconfirmedBoardInvitation, unconfirmedOrganizationInvitation,
          updateBoard, updateCard, updateCard:closed, updateCard:desc, updateCard:idList,
          updateCard:name, updateCheckItemStateOnCard, updateChecklist, updateList,
          updateList:closed, updateList:name, updateMember or updateOrganization'
      - in: query
        name: actions_display
        description: true or false
      - in: query
        name: actions_entities
        description: true or false
      - in: query
        name: actions_limit
        description: a number from 0 to 1000
      - in: query
        name: action_fields
        description: 'all or a comma-separated list of: data, date, idMemberCreator
          or type'
      - in: query
        name: boards
        description: 'all or a comma-separated list of: closed, members, open, organization,
          pinned, public, starred or unpinned'
      - in: query
        name: board_actions
        description: 'all or a comma-separated list of: addAttachmentToCard, addChecklistToCard,
          addMemberToBoard, addMemberToCard, addMemberToOrganization, addToOrganizationBoard,
          commentCard, convertToCardFromCheckItem, copyBoard, copyCard, copyCommentCard,
          createBoard, createCard, createList, createOrganization, deleteAttachmentFromCard,
          deleteBoardInvitation, deleteCard, deleteOrganizationInvitation, disablePowerUp,
          emailCard, enablePowerUp, makeAdminOfBoard, makeNormalMemberOfBoard, makeNormalMemberOfOrganization,
          makeObserverOfBoard, memberJoinedTrello, moveCardFromBoard, moveCardToBoard,
          moveListFromBoard, moveListToBoard, removeChecklistFromCard, removeFromOrganizationBoard,
          removeMemberFromCard, unconfirmedBoardInvitation, unconfirmedOrganizationInvitation,
          updateBoard, updateCard, updateCard:closed, updateCard:desc, updateCard:idList,
          updateCard:name, updateCheckItemStateOnCard, updateChecklist, updateList,
          updateList:closed, updateList:name, updateMember or updateOrganization'
      - in: query
        name: board_actions_display
        description: true or false
      - in: query
        name: board_actions_entities
        description: true or false
      - in: query
        name: board_actions_format
        description: 'One of: count, list or minimal'
      - in: query
        name: board_actions_limit
        description: a number from 0 to 1000
      - in: query
        name: board_actions_since
        description: A date, null or lastView
      - in: query
        name: board_action_fields
        description: 'all or a comma-separated list of: data, date, idMemberCreator
          or type'
      - in: query
        name: board_fields
        description: 'all or a comma-separated list of: closed, dateLastActivity,
          dateLastView, desc, descData, idOrganization, invitations, invited, labelNames,
          memberships, name, pinned, powerUps, prefs, shortLink, shortUrl, starred,
          subscribed or url'
      - in: query
        name: board_lists
        description: 'One of: all, closed, none or open'
      - in: query
        name: fields
        description: 'all or a comma-separated list of: billableMemberCount, desc,
          descData, displayName, idBoards, invitations, invited, logoHash, memberships,
          name, powerUps, prefs, premiumFeatures, products, url or website'
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: members
        description: 'One of: admins, all, none, normal or owners'
      - in: query
        name: memberships
        description: 'all or a comma-separated list of: active, admin, deactivated,
          me or normal'
      - in: query
        name: memberships_member
        description: true or false
      - in: query
        name: memberships_member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: membersInvited
        description: 'One of: admins, all, none, normal or owners'
      - in: query
        name: membersInvited_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: member_activity
        description: true or false ; works for premium organizations only
      - in: query
        name: member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: paid_account
        description: true or false
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
    put:
      summary: Put Organizations
      description: Put organizations.
      operationId: updateOrganizationsByIdOrg
      x-api-path-slug: organizationsidorg-put
      parameters:
      - in: body
        name: body
        description: Attributes of Organizations to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
  /organizations/{idOrg}/actions:
    get:
      summary: Get Organizations Actions
      description: Get organizations actions.
      operationId: getOrganizationsActionsByIdOrg
      x-api-path-slug: organizationsidorgactions-get
      parameters:
      - in: query
        name: before
        description: A date, or null
      - in: query
        name: display
        description: true or false
      - in: query
        name: entities
        description: true or false
      - in: query
        name: fields
        description: 'all or a comma-separated list of: data, date, idMemberCreator
          or type'
      - in: query
        name: filter
        description: 'all or a comma-separated list of: addAttachmentToCard, addChecklistToCard,
          addMemberToBoard, addMemberToCard, addMemberToOrganization, addToOrganizationBoard,
          commentCard, convertToCardFromCheckItem, copyBoard, copyCard, copyCommentCard,
          createBoard, createCard, createList, createOrganization, deleteAttachmentFromCard,
          deleteBoardInvitation, deleteCard, deleteOrganizationInvitation, disablePowerUp,
          emailCard, enablePowerUp, makeAdminOfBoard, makeNormalMemberOfBoard, makeNormalMemberOfOrganization,
          makeObserverOfBoard, memberJoinedTrello, moveCardFromBoard, moveCardToBoard,
          moveListFromBoard, moveListToBoard, removeChecklistFromCard, removeFromOrganizationBoard,
          removeMemberFromCard, unconfirmedBoardInvitation, unconfirmedOrganizationInvitation,
          updateBoard, updateCard, updateCard:closed, updateCard:desc, updateCard:idList,
          updateCard:name, updateCheckItemStateOnCard, updateChecklist, updateList,
          updateList:closed, updateList:name, updateMember or updateOrganization'
      - in: query
        name: format
        description: 'One of: count, list or minimal'
      - in: query
        name: idModels
        description: Only return actions related to these model ids
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: limit
        description: a number from 0 to 1000
      - in: query
        name: member
        description: true or false
      - in: query
        name: memberCreator
        description: true or false
      - in: query
        name: memberCreator_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: page
        description: Page * limit must be less than 1000
      - in: query
        name: since
        description: A date, null or lastView
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Actions
  /organizations/{idOrg}/boards:
    get:
      summary: Get Organizations Boards
      description: Get organizations boards.
      operationId: getOrganizationsBoardsByIdOrg
      x-api-path-slug: organizationsidorgboards-get
      parameters:
      - in: query
        name: actions
        description: 'all or a comma-separated list of: addAttachmentToCard, addChecklistToCard,
          addMemberToBoard, addMemberToCard, addMemberToOrganization, addToOrganizationBoard,
          commentCard, convertToCardFromCheckItem, copyBoard, copyCard, copyCommentCard,
          createBoard, createCard, createList, createOrganization, deleteAttachmentFromCard,
          deleteBoardInvitation, deleteCard, deleteOrganizationInvitation, disablePowerUp,
          emailCard, enablePowerUp, makeAdminOfBoard, makeNormalMemberOfBoard, makeNormalMemberOfOrganization,
          makeObserverOfBoard, memberJoinedTrello, moveCardFromBoard, moveCardToBoard,
          moveListFromBoard, moveListToBoard, removeChecklistFromCard, removeFromOrganizationBoard,
          removeMemberFromCard, unconfirmedBoardInvitation, unconfirmedOrganizationInvitation,
          updateBoard, updateCard, updateCard:closed, updateCard:desc, updateCard:idList,
          updateCard:name, updateCheckItemStateOnCard, updateChecklist, updateList,
          updateList:closed, updateList:name, updateMember or updateOrganization'
      - in: query
        name: actions_entities
        description: true or false
      - in: query
        name: actions_format
        description: 'One of: count, list or minimal'
      - in: query
        name: actions_limit
        description: a number from 0 to 1000
      - in: query
        name: actions_since
        description: A date, null or lastView
      - in: query
        name: action_fields
        description: 'all or a comma-separated list of: data, date, idMemberCreator
          or type'
      - in: query
        name: fields
        description: 'all or a comma-separated list of: closed, dateLastActivity,
          dateLastView, desc, descData, idOrganization, invitations, invited, labelNames,
          memberships, name, pinned, powerUps, prefs, shortLink, shortUrl, starred,
          subscribed or url'
      - in: query
        name: filter
        description: 'all or a comma-separated list of: closed, members, open, organization,
          pinned, public, starred or unpinned'
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: lists
        description: 'One of: all, closed, none or open'
      - in: query
        name: memberships
        description: 'all or a comma-separated list of: active, admin, deactivated,
          me or normal'
      - in: query
        name: organization
        description: true or false
      - in: query
        name: organization_fields
        description: 'all or a comma-separated list of: billableMemberCount, desc,
          descData, displayName, idBoards, invitations, invited, logoHash, memberships,
          name, powerUps, prefs, premiumFeatures, products, url or website'
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Boards
  /organizations/{idOrg}/boards/{filter}:
    get:
      summary: Get Organizations Boards Filter
      description: Get organizations boards filter.
      operationId: getOrganizationsBoardsByIdOrgByFilter
      x-api-path-slug: organizationsidorgboardsfilter-get
      parameters:
      - in: path
        name: filter
        description: filter
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Boards
      - Filter
  /organizations/{idOrg}/deltas:
    get:
      summary: Get Organizations Deltas
      description: Get organizations deltas.
      operationId: getOrganizationsDeltasByIdOrg
      x-api-path-slug: organizationsidorgdeltas-get
      parameters:
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: ixLastUpdate
        description: a number from -1 to Infinity
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: tags
        description: A valid tag for subscribing
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Deltas
  /organizations/{idOrg}/desc:
    put:
      summary: Put Organizations Desc
      description: Put organizations desc.
      operationId: updateOrganizationsDescByIdOrg
      x-api-path-slug: organizationsidorgdesc-put
      parameters:
      - in: body
        name: body
        description: Attributes of Organizations Desc to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Desc
  /organizations/{idOrg}/displayName:
    put:
      summary: Put Organizations Displayname
      description: Put organizations displayname.
      operationId: updateOrganizationsDisplayNameByIdOrg
      x-api-path-slug: organizationsidorgdisplayname-put
      parameters:
      - in: body
        name: body
        description: Attributes of Organizations Display Name to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Displayname
  /organizations/{idOrg}/logo:
    delete:
      summary: Delete Organizations Logo
      description: Delete organizations logo.
      operationId: deleteOrganizationsLogoByIdOrg
      x-api-path-slug: organizationsidorglogo-delete
      parameters:
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Logo
    post:
      summary: Post Organizations Logo
      description: Post organizations logo.
      operationId: addOrganizationsLogoByIdOrg
      x-api-path-slug: organizationsidorglogo-post
      parameters:
      - in: body
        name: body
        description: Attributes of Organizations Logo to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Logo
  /organizations/{idOrg}/members:
    get:
      summary: Get Organizations Members
      description: Get organizations members.
      operationId: getOrganizationsMembersByIdOrg
      x-api-path-slug: organizationsidorgmembers-get
      parameters:
      - in: query
        name: activity
        description: true or false ; works for premium organizations only
      - in: query
        name: fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: filter
        description: 'One of: admins, all, none, normal or owners'
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Members
    put:
      summary: Put Organizations Members
      description: Put organizations members.
      operationId: updateOrganizationsMembersByIdOrg
      x-api-path-slug: organizationsidorgmembers-put
      parameters:
      - in: body
        name: body
        description: Attributes of Organizations Members to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Members
  /organizations/{idOrg}/members/{filter}:
    get:
      summary: Get Organizations Members Filter
      description: Get organizations members filter.
      operationId: getOrganizationsMembersByIdOrgByFilter
      x-api-path-slug: organizationsidorgmembersfilter-get
      parameters:
      - in: path
        name: filter
        description: filter
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Members
      - Filter
  /organizations/{idOrg}/members/{idMember}:
    delete:
      summary: Delete Organizations Members
      description: Delete organizations members.
      operationId: deleteOrganizationsMembersByIdOrgByIdMember
      x-api-path-slug: organizationsidorgmembersidmember-delete
      parameters:
      - in: path
        name: idMember
        description: idMember
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Members
    put:
      summary: Put Organizations Members
      description: Put organizations members.
      operationId: updateOrganizationsMembersByIdOrgByIdMember
      x-api-path-slug: organizationsidorgmembersidmember-put
      parameters:
      - in: body
        name: body
        description: Attributes of Organizations Members to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Members
  /organizations/{idOrg}/members/{idMember}/all:
    delete:
      summary: Delete Organizations Members All
      description: Delete organizations members all.
      operationId: deleteOrganizationsMembersAllByIdOrgByIdMember
      x-api-path-slug: organizationsidorgmembersidmemberall-delete
      parameters:
      - in: path
        name: idMember
        description: idMember
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Members
  /organizations/{idOrg}/members/{idMember}/cards:
    get:
      summary: Get Organizations Members Cards
      description: Get organizations members cards.
      operationId: getOrganizationsMembersCardsByIdOrgByIdMember
      x-api-path-slug: organizationsidorgmembersidmembercards-get
      parameters:
      - in: query
        name: actions
        description: 'all or a comma-separated list of: addAttachmentToCard, addChecklistToCard,
          addMemberToBoard, addMemberToCard, addMemberToOrganization, addToOrganizationBoard,
          commentCard, convertToCardFromCheckItem, copyBoard, copyCard, copyCommentCard,
          createBoard, createCard, createList, createOrganization, deleteAttachmentFromCard,
          deleteBoardInvitation, deleteCard, deleteOrganizationInvitation, disablePowerUp,
          emailCard, enablePowerUp, makeAdminOfBoard, makeNormalMemberOfBoard, makeNormalMemberOfOrganization,
          makeObserverOfBoard, memberJoinedTrello, moveCardFromBoard, moveCardToBoard,
          moveListFromBoard, moveListToBoard, removeChecklistFromCard, removeFromOrganizationBoard,
          removeMemberFromCard, unconfirmedBoardInvitation, unconfirmedOrganizationInvitation,
          updateBoard, updateCard, updateCard:closed, updateCard:desc, updateCard:idList,
          updateCard:name, updateCheckItemStateOnCard, updateChecklist, updateList,
          updateList:closed, updateList:name, updateMember or updateOrganization'
      - in: query
        name: attachments
        description: A boolean value or &quot;cover&quot; for only card cover attachments
      - in: query
        name: attachment_fields
        description: 'all or a comma-separated list of: bytes, date, edgeColor, idMember,
          isUpload, mimeType, name, previews or url'
      - in: query
        name: board
        description: true or false
      - in: query
        name: board_fields
        description: 'all or a comma-separated list of: closed, dateLastActivity,
          dateLastView, desc, descData, idOrganization, invitations, invited, labelNames,
          memberships, name, pinned, powerUps, prefs, shortLink, shortUrl, starred,
          subscribed or url'
      - in: query
        name: checkItemStates
        description: true or false
      - in: query
        name: checklists
        description: 'One of: all or none'
      - in: query
        name: fields
        description: 'all or a comma-separated list of: badges, checkItemStates, closed,
          dateLastActivity, desc, descData, due, email, idAttachmentCover, idBoard,
          idChecklists, idLabels, idList, idMembers, idMembersVoted, idShort, labels,
          manualCoverAttachment, name, pos, shortLink, shortUrl, subscribed or url'
      - in: query
        name: filter
        description: 'One of: all, closed, none, open or visible'
      - in: path
        name: idMember
        description: idMember
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: list
        description: true or false
      - in: query
        name: list_fields
        description: 'all or a comma-separated list of: closed, idBoard, name, pos
          or subscribed'
      - in: query
        name: members
        description: true or false
      - in: query
        name: member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Members
      - Cards
  /organizations/{idOrg}/members/{idMember}/deactivated:
    put:
      summary: Put Organizations Members Deactivated
      description: Put organizations members deactivated.
      operationId: updateOrganizationsMembersDeactivatedByIdOrgByIdMember
      x-api-path-slug: organizationsidorgmembersidmemberdeactivated-put
      parameters:
      - in: body
        name: body
        description: Attributes of Organizations Members Deactivated to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Members
      - Deactivated
  /organizations/{idOrg}/membersInvited:
    get:
      summary: Get Organizations Membersinvited
      description: Get organizations membersinvited.
      operationId: getOrganizationsMembersInvitedByIdOrg
      x-api-path-slug: organizationsidorgmembersinvited-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: avatarHash, avatarSource,
          bio, bioData, confirmed, email, fullName, gravatarHash, idBoards, idBoardsPinned,
          idOrganizations, idPremOrgsAdmin, initials, loginTypes, memberType, oneTimeMessagesDismissed,
          prefs, premiumFeatures, products, status, status, trophies, uploadedAvatarHash,
          url or username'
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Membersinvited
  /organizations/{idOrg}/membersInvited/{field}:
    get:
      summary: Get Organizations Membersinvited Field
      description: Get organizations membersinvited field.
      operationId: getOrganizationsMembersInvitedByIdOrgByField
      x-api-path-slug: organizationsidorgmembersinvitedfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Membersinvited
      - Field
  /organizations/{idOrg}/memberships:
    get:
      summary: Get Organizations Memberships
      description: Get organizations memberships.
      operationId: getOrganizationsMembershipsByIdOrg
      x-api-path-slug: organizationsidorgmemberships-get
      parameters:
      - in: query
        name: filter
        description: 'all or a comma-separated list of: active, admin, deactivated,
          me or normal'
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: member
        description: true or false
      - in: query
        name: member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Memberships
  /organizations/{idOrg}/memberships/{idMembership}:
    get:
      summary: Get Organizations Memberships
      description: Get organizations memberships.
      operationId: getOrganizationsMembershipsByIdOrgByIdMembership
      x-api-path-slug: organizationsidorgmembershipsidmembership-get
      parameters:
      - in: path
        name: idMembership
        description: idMembership
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: member
        description: true or false
      - in: query
        name: member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Memberships
    put:
      summary: Put Organizations Memberships
      description: Put organizations memberships.
      operationId: updateOrganizationsMembershipsByIdOrgByIdMembership
      x-api-path-slug: organizationsidorgmembershipsidmembership-put
      parameters:
      - in: body
        name: body
        description: Attributes of Organizations Memberships to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMembership
        description: idMembership
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Memberships
  /organizations/{idOrg}/name:
    put:
      summary: Put Organizations Name
      description: Put organizations name.
      operationId: updateOrganizationsNameByIdOrg
      x-api-path-slug: organizationsidorgname-put
      parameters:
      - in: body
        name: body
        description: Attributes of Organizations Name to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Name
  /organizations/{idOrg}/prefs/associatedDomain:
    delete:
      summary: Delete Organizations Preferences Associateddomain
      description: Delete organizations preferences associateddomain.
      operationId: deleteOrganizationsPrefsAssociatedDomainByIdOrg
      x-api-path-slug: organizationsidorgprefsassociateddomain-delete
      parameters:
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Preferences
      - Associateddomain
    put:
      summary: Put Organizations Preferences Associateddomain
      description: Put organizations preferences associateddomain.
      operationId: updateOrganizationsPrefsAssociatedDomainByIdOrg
      x-api-path-slug: organizationsidorgprefsassociateddomain-put
      parameters:
      - in: body
        name: body
        description: Attributes of Prefs Associated Domain to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Preferences
      - Associateddomain
  /organizations/{idOrg}/prefs/boardVisibilityRestrict/org:
    put:
      summary: Put Organizations Preferences Boardvisibilityrestrict Org
      description: Put organizations preferences boardvisibilityrestrict org.
      operationId: updateOrganizationsPrefsBoardVisibilityRestrictOrgByIdOrg
      x-api-path-slug: organizationsidorgprefsboardvisibilityrestrictorg-put
      parameters:
      - in: body
        name: body
        description: Attributes of Prefs Board Visibility Restrict to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Preferences
      - Boardvisibilityrestrict
      - Org
  /organizations/{idOrg}/prefs/boardVisibilityRestrict/private:
    put:
      summary: Put Organizations Preferences Boardvisibilityrestrict Private
      description: Put organizations preferences boardvisibilityrestrict private.
      operationId: updateOrganizationsPrefsBoardVisibilityRestrictPrivateByIdOrg
      x-api-path-slug: organizationsidorgprefsboardvisibilityrestrictprivate-put
      parameters:
      - in: body
        name: body
        description: Attributes of Prefs Board Visibility Restrict to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Preferences
      - Boardvisibilityrestrict
      - Private
  /organizations/{idOrg}/prefs/boardVisibilityRestrict/public:
    put:
      summary: Put Organizations Preferences Boardvisibilityrestrict Public
      description: Put organizations preferences boardvisibilityrestrict public.
      operationId: updateOrganizationsPrefsBoardVisibilityRestrictPublicByIdOrg
      x-api-path-slug: organizationsidorgprefsboardvisibilityrestrictpublic-put
      parameters:
      - in: body
        name: body
        description: Attributes of Prefs Board Visibility Restrict to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Preferences
      - Boardvisibilityrestrict
      - Public
  /organizations/{idOrg}/prefs/externalMembersDisabled:
    put:
      summary: Put Organizations Preferences Externalmembersdisabled
      description: Put organizations preferences externalmembersdisabled.
      operationId: updateOrganizationsPrefsExternalMembersDisabledByIdOrg
      x-api-path-slug: organizationsidorgprefsexternalmembersdisabled-put
      parameters:
      - in: body
        name: body
        description: Attributes of Prefs External Members Disabled to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Preferences
      - Externalmembersdisabled
  /organizations/{idOrg}/prefs/googleAppsVersion:
    put:
      summary: Put Organizations Preferences Googleappsversion
      description: Put organizations preferences googleappsversion.
      operationId: updateOrganizationsPrefsGoogleAppsVersionByIdOrg
      x-api-path-slug: organizationsidorgprefsgoogleappsversion-put
      parameters:
      - in: body
        name: body
        description: Attributes of Prefs Google Apps Version to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Preferences
      - Googleappsversion
  /organizations/{idOrg}/prefs/orgInviteRestrict:
    delete:
      summary: Delete Organizations Preferences Orginviterestrict
      description: Delete organizations preferences orginviterestrict.
      operationId: deleteOrganizationsPrefsOrgInviteRestrictByIdOrg
      x-api-path-slug: organizationsidorgprefsorginviterestrict-delete
      parameters:
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      - in: query
        name: value
        description: An email address with optional expansion tokens
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Preferences
      - Orginviterestrict
    put:
      summary: Put Organizations Preferences Orginviterestrict
      description: Put organizations preferences orginviterestrict.
      operationId: updateOrganizationsPrefsOrgInviteRestrictByIdOrg
      x-api-path-slug: organizationsidorgprefsorginviterestrict-put
      parameters:
      - in: body
        name: body
        description: Attributes of Prefs Org Invite Restrict to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Preferences
      - Orginviterestrict
  /organizations/{idOrg}/prefs/permissionLevel:
    put:
      summary: Put Organizations Preferences Permissionlevel
      description: Put organizations preferences permissionlevel.
      operationId: updateOrganizationsPrefsPermissionLevelByIdOrg
      x-api-path-slug: organizationsidorgprefspermissionlevel-put
      parameters:
      - in: body
        name: body
        description: Attributes of Prefs Permission Level to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Preferences
      - Permissionlevel
  /organizations/{idOrg}/website:
    put:
      summary: Put Organizations Website
      description: Put organizations website.
      operationId: updateOrganizationsWebsiteByIdOrg
      x-api-path-slug: organizationsidorgwebsite-put
      parameters:
      - in: body
        name: body
        description: Attributes of Organizations Website to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Website
  /organizations/{idOrg}/{field}:
    get:
      summary: Get Organizations Field
      description: Get organizations field.
      operationId: getOrganizationsByIdOrgByField
      x-api-path-slug: organizationsidorgfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Field
  /search:
    get:
      summary: Get Search
      description: Get search.
      operationId: getSearch
      x-api-path-slug: search-get
      parameters:
      - in: query
        name: boards_limit
        description: a number from 1 to 1000
      - in: query
        name: board_fields
        description: 'all or a comma-separated list of: closed, dateLastActivity,
          dateLastView, desc, descData, idOrganization, invitations, invited, labelNames,
          memberships, name, pinned, powerUps, prefs, shortLink, shortUrl, starred,
          subscribed or url'
      - in: query
        name: cards_limit
        description: a number from 1 to 1000
      - in: query
        name: cards_page
        description: a number from 0 to 100
      - in: query
        name: card_attachments
        description: A boolean value or &quot;cover&quot; for only card cover attachments
      - in: query
        name: card_board
        description: true or false
      - in: query
        name: card_fields
        description: 'all or a comma-separated list of: badges, checkItemStates, closed,
          dateLastActivity, desc, descData, due, email, idAttachmentCover, idBoard,
          idChecklists, idLabels, idList, idMembers, idMembersVoted, idShort, labels,
          manualCoverAttachment, name, pos, shortLink, shortUrl, subscribed or url'
      - in: query
        name: card_list
        description: true or false
      - in: query
        name: card_members
        description: true or false
      - in: query
        name: card_stickers
        description: true or false
      - in: query
        name: idBoards
        description: A comma-separated list of objectIds, 24-character hex strings
      - in: query
        name: idCards
        description: A comma-separated list of objectIds, 24-character hex strings
      - in: query
        name: idOrganizations
        description: A comma-separated list of objectIds, 24-character hex strings
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: members_limit
        description: a number from 1 to 1000
      - in: query
        name: member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: modelTypes
        description: 'all or a comma-separated list of: actions, boards, cards, members
          or organizations'
      - in: query
        name: organizations_limit
        description: a number from 1 to 1000
      - in: query
        name: organization_fields
        description: 'all or a comma-separated list of: billableMemberCount, desc,
          descData, displayName, idBoards, invitations, invited, logoHash, memberships,
          name, powerUps, prefs, premiumFeatures, products, url or website'
      - in: query
        name: partial
        description: true or false
      - in: query
        name: query
        description: a string with a length from 1 to 16384
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Search
  /search/members:
    get:
      summary: Get Search Members
      description: Get search members.
      operationId: getSearchMembers
      x-api-path-slug: searchmembers-get
      parameters:
      - in: query
        name: idBoard
        description: An id, or null
      - in: query
        name: idOrganization
        description: An id, or null
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: limit
        description: a number from 1 to 20
      - in: query
        name: onlyOrgMembers
        description: A boolean
      - in: query
        name: query
        description: a string with a length from 1 to 16384
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Search
      - Members
  /sessions:
    post:
      summary: Post Sessions
      description: Post sessions.
      operationId: addSessions
      x-api-path-slug: sessions-post
      parameters:
      - in: body
        name: body
        description: Attributes of Sessions to be added
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Sessions
  /sessions/socket:
    get:
      summary: Get Sessions Socket
      description: Get sessions socket.
      operationId: getSessionsSocket
      x-api-path-slug: sessionssocket-get
      parameters:
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Sessions
      - Socket
  /sessions/{idSession}:
    put:
      summary: Put Sessions
      description: Put sessions.
      operationId: updateSessionsByIdSession
      x-api-path-slug: sessionsidsession-put
      parameters:
      - in: body
        name: body
        description: Attributes of Sessions to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idSession
        description: idSession
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Sessions
  /sessions/{idSession}/status:
    put:
      summary: Put Sessions Status
      description: Put sessions status.
      operationId: updateSessionsStatusByIdSession
      x-api-path-slug: sessionsidsessionstatus-put
      parameters:
      - in: body
        name: body
        description: Attributes of Sessions Status to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idSession
        description: idSession
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Sessions
      - Status
  /tokens/{token}:
    delete:
      summary: Delete Tokens
      description: Delete tokens.
      operationId: deleteTokensByToken
      x-api-path-slug: tokenstoken-delete
      parameters:
      - in: query
        name: key
        description: Generate your application key
      - in: path
        name: token
        description: token
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Tokens
    get:
      summary: Get Tokens
      description: Get tokens.
      operationId: getTokensByToken
      x-api-path-slug: tokenstoken-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: dateCreated, dateExpires,
          idMember, identifier or permissions'
      - in: query
        name: key
        description: Generate your application key
      - in: path
        name: token
        description: token
      - in: query
        name: token
        description: Getting a token from a user
      - in: query
        name: webhooks
        description: true or false
      responses:
        200:
          description: OK
      tags:
      - Tokens
  /tokens/{token}/member:
    get:
      summary: Get Tokens Member
      description: Get tokens member.
      operationId: getTokensMemberByToken
      x-api-path-slug: tokenstokenmember-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: avatarHash, avatarSource,
          bio, bioData, confirmed, email, fullName, gravatarHash, idBoards, idBoardsPinned,
          idOrganizations, idPremOrgsAdmin, initials, loginTypes, memberType, oneTimeMessagesDismissed,
          prefs, premiumFeatures, products, status, status, trophies, uploadedAvatarHash,
          url or username'
      - in: query
        name: key
        description: Generate your application key
      - in: path
        name: token
        description: token
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Tokens
      - Member
  /tokens/{token}/member/{field}:
    get:
      summary: Get Tokens Member Field
      description: Get tokens member field.
      operationId: getTokensMemberByTokenByField
      x-api-path-slug: tokenstokenmemberfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: query
        name: key
        description: Generate your application key
      - in: path
        name: token
        description: token
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Tokens
      - Member
      - Field
  /tokens/{token}/webhooks:
    get:
      summary: Get Tokens Webhooks
      description: Get tokens webhooks.
      operationId: getTokensWebhooksByToken
      x-api-path-slug: tokenstokenwebhooks-get
      parameters:
      - in: query
        name: key
        description: Generate your application key
      - in: path
        name: token
        description: token
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Tokens
      - Webhooks
    post:
      summary: Post Tokens Webhooks
      description: Post tokens webhooks.
      operationId: addTokensWebhooksByToken
      x-api-path-slug: tokenstokenwebhooks-post
      parameters:
      - in: body
        name: body
        description: Attributes of Tokens Webhooks to be added
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: key
        description: Generate your application key
      - in: path
        name: token
        description: token
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Tokens
      - Webhooks
    put:
      summary: Put Tokens Webhooks
      description: Put tokens webhooks.
      operationId: updateTokensWebhooksByToken
      x-api-path-slug: tokenstokenwebhooks-put
      parameters:
      - in: body
        name: body
        description: Attributes of Tokens Webhooks to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: key
        description: Generate your application key
      - in: path
        name: token
        description: token
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Tokens
      - Webhooks
  /tokens/{token}/webhooks/{idWebhook}:
    delete:
      summary: Delete Tokens Webhooks
      description: Delete tokens webhooks.
      operationId: deleteTokensWebhooksByTokenByIdWebhook
      x-api-path-slug: tokenstokenwebhooksidwebhook-delete
      parameters:
      - in: path
        name: idWebhook
        description: idWebhook
      - in: query
        name: key
        description: Generate your application key
      - in: path
        name: token
        description: token
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Tokens
      - Webhooks
    get:
      summary: Get Tokens Webhooks
      description: Get tokens webhooks.
      operationId: getTokensWebhooksByTokenByIdWebhook
      x-api-path-slug: tokenstokenwebhooksidwebhook-get
      parameters:
      - in: path
        name: idWebhook
        description: idWebhook
      - in: query
        name: key
        description: Generate your application key
      - in: path
        name: token
        description: token
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Tokens
      - Webhooks
  /tokens/{token}/{field}:
    get:
      summary: Get Tokens Field
      description: Get tokens field.
      operationId: getTokensByTokenByField
      x-api-path-slug: tokenstokenfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: query
        name: key
        description: Generate your application key
      - in: path
        name: token
        description: token
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Tokens
      - Field
  /types/{id}:
    get:
      summary: Get Types
      description: Get types.
      operationId: getTypesById
      x-api-path-slug: typesid-get
      parameters:
      - in: path
        name: id
        description: id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Types
  /webhooks:
    post:
      summary: Post Webhooks
      description: Post webhooks.
      operationId: addWebhooks
      x-api-path-slug: webhooks-post
      parameters:
      - in: body
        name: body
        description: Attributes of Webhooks to be added
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Webhooks
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---