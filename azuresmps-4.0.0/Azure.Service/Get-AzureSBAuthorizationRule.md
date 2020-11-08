---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D7B2CDFF-D9A2-48C7-B331-132A6A6843CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 10fdb8920164857b42ac57a3c989417c2a967ab9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023572"
---
# <span data-ttu-id="6af7c-101">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6af7c-101">Get-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="6af7c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6af7c-102">SYNOPSIS</span></span>
<span data-ttu-id="6af7c-103">Ottiene le regole di autorizzazione di Service Bus.</span><span class="sxs-lookup"><span data-stu-id="6af7c-103">Gets Service bus authorization rules.</span></span>


## <span data-ttu-id="6af7c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6af7c-104">SYNTAX</span></span>

### <span data-ttu-id="6af7c-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="6af7c-105">EntitySAS</span></span>
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6af7c-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="6af7c-106">NamespaceSAS</span></span>
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6af7c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6af7c-107">DESCRIPTION</span></span>
<span data-ttu-id="6af7c-108">Ottiene le regole di autorizzazione di Service Bus.</span><span class="sxs-lookup"><span data-stu-id="6af7c-108">Gets Service bus authorization rules.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="6af7c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6af7c-109">EXAMPLES</span></span>

### <span data-ttu-id="6af7c-110">Esempio 1: ottenere la regola di autorizzazione al livello dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6af7c-110">Example 1: Get authorization rule at namespace level</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace
```

<span data-ttu-id="6af7c-111">Ottiene tutte le regole di autorizzazione disponibili in MyNamespace.</span><span class="sxs-lookup"><span data-stu-id="6af7c-111">Gets all available authorization rules at MyNamespace.</span></span>

### <span data-ttu-id="6af7c-112">Esempio 2: ottenere la regola di autorizzazione per una coda</span><span class="sxs-lookup"><span data-stu-id="6af7c-112">Example 2: Get authorization rule for a Queue</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="6af7c-113">Ottiene tutte le regole di autorizzazione disponibili una coda di entità in MyNamespace.</span><span class="sxs-lookup"><span data-stu-id="6af7c-113">Gets all available authorization rules a MyEntity Queue on MyNamespace.</span></span>

### <span data-ttu-id="6af7c-114">Esempio 3: ottenere la regola di autorizzazione per nome</span><span class="sxs-lookup"><span data-stu-id="6af7c-114">Example 3: Get authorization rule by name</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace
```

<span data-ttu-id="6af7c-115">Ottiene una regola di autorizzazione chiamata regola del livello di spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6af7c-115">Gets an authorization rule called MyRule on MyNamespace level.</span></span>

### <span data-ttu-id="6af7c-116">Esempio 4: ottenere la regola di autorizzazione tramite autorizzazione</span><span class="sxs-lookup"><span data-stu-id="6af7c-116">Example 4: Get authorization rule by permission</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="6af7c-117">Ottiene tutte le regole di autorizzazione che hanno l'autorizzazione di invio sul livello dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6af7c-117">Gets all authorization rules that have send permission on namespace level.</span></span>

## <span data-ttu-id="6af7c-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6af7c-118">PARAMETERS</span></span>

### <span data-ttu-id="6af7c-119">-EntityName</span><span class="sxs-lookup"><span data-stu-id="6af7c-119">-EntityName</span></span>
<span data-ttu-id="6af7c-120">Nome dell'entità a cui applicare la regola.</span><span class="sxs-lookup"><span data-stu-id="6af7c-120">The entity name to apply rule at.</span></span>

```yaml
Type: String
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6af7c-121">-EntityType</span><span class="sxs-lookup"><span data-stu-id="6af7c-121">-EntityType</span></span>
<span data-ttu-id="6af7c-122">Il tipo di entità (Queue, Topic, Relay, NotificationHub).</span><span class="sxs-lookup"><span data-stu-id="6af7c-122">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

```yaml
Type: ServiceBusEntityType
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6af7c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="6af7c-123">-Name</span></span>
<span data-ttu-id="6af7c-124">Nome della regola di autorizzazione univoco.</span><span class="sxs-lookup"><span data-stu-id="6af7c-124">The unique authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6af7c-125">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6af7c-125">-Namespace</span></span>
<span data-ttu-id="6af7c-126">Nome dello spazio dei nomi per applicare la regola di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="6af7c-126">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="6af7c-127">Se nessun EntityName ha specificato che la regola sarà sul livello dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6af7c-127">If no EntityName provided the rule will be on the namespace level.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6af7c-128">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="6af7c-128">-Permission</span></span>
<span data-ttu-id="6af7c-129">Autorizzazioni di autorizzazione per filtrare (Invia, Gestisci, ascolta).</span><span class="sxs-lookup"><span data-stu-id="6af7c-129">The authorization permissions to filter (Send, Manage, Listen).</span></span>
<span data-ttu-id="6af7c-130">Questo usa la corrispondenza esatta.</span><span class="sxs-lookup"><span data-stu-id="6af7c-130">This uses exact match.</span></span>

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6af7c-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="6af7c-131">-Profile</span></span>
<span data-ttu-id="6af7c-132">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6af7c-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6af7c-133">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="6af7c-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6af7c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6af7c-134">CommonParameters</span></span>
<span data-ttu-id="6af7c-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6af7c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6af7c-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6af7c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6af7c-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6af7c-137">INPUTS</span></span>

## <span data-ttu-id="6af7c-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6af7c-138">OUTPUTS</span></span>

## <span data-ttu-id="6af7c-139">Note</span><span class="sxs-lookup"><span data-stu-id="6af7c-139">NOTES</span></span>

## <span data-ttu-id="6af7c-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6af7c-140">RELATED LINKS</span></span>

[<span data-ttu-id="6af7c-141">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6af7c-141">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="6af7c-142">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6af7c-142">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)

[<span data-ttu-id="6af7c-143">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6af7c-143">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


