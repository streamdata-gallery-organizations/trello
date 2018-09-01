---
swagger: "2.0"
x-collection-name: Trello
x-complete: 0
info:
  title: Trello Post Members Boardbackgrounds
  description: Post members boardbackgrounds.
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