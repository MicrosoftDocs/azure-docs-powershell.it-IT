---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 17065902-97EA-4F5F-926B-B7CBEE3EAF84
online version: ''
schema: 2.0.0
ms.openlocfilehash: ab76cf3052f28b0ff89e3e41aaa08127cc33411e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023778"
---
# <span data-ttu-id="9bebf-101">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9bebf-101">Set-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="9bebf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9bebf-102">SYNOPSIS</span></span>
<span data-ttu-id="9bebf-103">Aggiorna la regola di autorizzazione di Service Bus esistente.</span><span class="sxs-lookup"><span data-stu-id="9bebf-103">Updates existing Service Bus authorization rule.</span></span>

## <span data-ttu-id="9bebf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9bebf-104">SYNTAX</span></span>

### <span data-ttu-id="9bebf-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="9bebf-105">EntitySAS</span></span>
```
Set-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9bebf-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="9bebf-106">NamespaceSAS</span></span>
```
Set-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9bebf-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bebf-107">DESCRIPTION</span></span>
<span data-ttu-id="9bebf-108">Aggiorna la regola di autorizzazione di Service Bus esistente.</span><span class="sxs-lookup"><span data-stu-id="9bebf-108">Updates existing Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="9bebf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9bebf-109">EXAMPLES</span></span>

### <span data-ttu-id="9bebf-110">Esempio 1: rinnovare la chiave primaria per la regola di autorizzazione a livello di spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9bebf-110">Example 1: Renew primary key for authorization rule at namespace level</span></span>
```
PS C:\> Set-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="9bebf-111">La chiave primaria viene rinnovata.</span><span class="sxs-lookup"><span data-stu-id="9bebf-111">The primary key is renewed.</span></span>

### <span data-ttu-id="9bebf-112">Esempio 2: autorizzazione Aggiorna regola di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="9bebf-112">Example 2: Update authorization rule permission</span></span>
```
PS C:\> Set-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Listen", "Send") -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="9bebf-113">Aggiorna le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="9bebf-113">Updates the permissions.</span></span>

## <span data-ttu-id="9bebf-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9bebf-114">PARAMETERS</span></span>

### <span data-ttu-id="9bebf-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="9bebf-115">-EntityName</span></span>
<span data-ttu-id="9bebf-116">Nome dell'entità a cui applicare la regola.</span><span class="sxs-lookup"><span data-stu-id="9bebf-116">The entity name to apply rule at.</span></span>

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

### <span data-ttu-id="9bebf-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="9bebf-117">-EntityType</span></span>
<span data-ttu-id="9bebf-118">Il tipo di entità (Queue, Topic, Relay, NotificationHub).</span><span class="sxs-lookup"><span data-stu-id="9bebf-118">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

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

### <span data-ttu-id="9bebf-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="9bebf-119">-Name</span></span>
<span data-ttu-id="9bebf-120">Nome della regola di autorizzazione univoco.</span><span class="sxs-lookup"><span data-stu-id="9bebf-120">The unique authorization rule name.</span></span>

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

### <span data-ttu-id="9bebf-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9bebf-121">-Namespace</span></span>
<span data-ttu-id="9bebf-122">Nome dello spazio dei nomi per applicare la regola di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="9bebf-122">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="9bebf-123">Se nessun EntityName ha specificato che la regola sarà sul livello dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="9bebf-123">If no EntityName provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="9bebf-124">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="9bebf-124">-Permission</span></span>
<span data-ttu-id="9bebf-125">Autorizzazioni di autorizzazione (Invia, Gestisci, ascolta).</span><span class="sxs-lookup"><span data-stu-id="9bebf-125">The authorization permissions (Send, Manage, Listen).</span></span>

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bebf-126">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="9bebf-126">-PrimaryKey</span></span>
<span data-ttu-id="9bebf-127">Chiave primaria della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="9bebf-127">The Shared Access Signature primary key.</span></span>
<span data-ttu-id="9bebf-128">Verrà generato se non specificato.</span><span class="sxs-lookup"><span data-stu-id="9bebf-128">Will be generated if not provided.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bebf-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="9bebf-129">-Profile</span></span>
<span data-ttu-id="9bebf-130">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bebf-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9bebf-131">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="9bebf-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9bebf-132">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="9bebf-132">-SecondaryKey</span></span>
<span data-ttu-id="9bebf-133">Chiave secondaria della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="9bebf-133">The Shared Access Signature secondary key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bebf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bebf-134">CommonParameters</span></span>
<span data-ttu-id="9bebf-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bebf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bebf-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bebf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bebf-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9bebf-137">INPUTS</span></span>

## <span data-ttu-id="9bebf-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9bebf-138">OUTPUTS</span></span>

## <span data-ttu-id="9bebf-139">Note</span><span class="sxs-lookup"><span data-stu-id="9bebf-139">NOTES</span></span>

## <span data-ttu-id="9bebf-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9bebf-140">RELATED LINKS</span></span>

[<span data-ttu-id="9bebf-141">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9bebf-141">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="9bebf-142">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9bebf-142">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="9bebf-143">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9bebf-143">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)


