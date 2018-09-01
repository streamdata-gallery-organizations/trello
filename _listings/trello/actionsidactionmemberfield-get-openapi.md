---
swagger: "2.0"
x-collection-name: Trello
x-complete: 0
info:
  title: Trello Get Actions Member Field
  description: Get actions member field.
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