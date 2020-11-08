---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 75320133-E7B1-40D4-B16D-567686D5AE99
online version: ''
schema: 2.0.0
ms.openlocfilehash: 40d3bdc73ce6bcbb199cf99bb0586de52f05e132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023945"
---
# <span data-ttu-id="c478b-101">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c478b-101">New-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="c478b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c478b-102">SYNOPSIS</span></span>
<span data-ttu-id="c478b-103">Crea la nuova regola di autorizzazione di Service Bus.</span><span class="sxs-lookup"><span data-stu-id="c478b-103">Creates new Service Bus authorization rule.</span></span>

## <span data-ttu-id="c478b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c478b-104">SYNTAX</span></span>

### <span data-ttu-id="c478b-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="c478b-105">EntitySAS</span></span>
```
New-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c478b-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="c478b-106">NamespaceSAS</span></span>
```
New-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c478b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c478b-107">DESCRIPTION</span></span>
<span data-ttu-id="c478b-108">Il cmdlet **New-AzureSBAuthorizationRule** crea una regola di autorizzazione di Service Bus.</span><span class="sxs-lookup"><span data-stu-id="c478b-108">The **New-AzureSBAuthorizationRule** cmdlet creates a Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="c478b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c478b-109">EXAMPLES</span></span>

### <span data-ttu-id="c478b-110">Esempio 1: creare una regola di autorizzazione con la chiave primaria generata</span><span class="sxs-lookup"><span data-stu-id="c478b-110">Example 1: Create an authorization rule with generated primary key</span></span>
```
PS C:\> New-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="c478b-111">Crea una nuova regola di autorizzazione sul livello dello spazio dei nomi con l'autorizzazione di invio.</span><span class="sxs-lookup"><span data-stu-id="c478b-111">Creates new authorization rule on namespace level with Send permission.</span></span>

### <span data-ttu-id="c478b-112">Esempio 2: crea una regola di autorizzazione fornendo la chiave primaria</span><span class="sxs-lookup"><span data-stu-id="c478b-112">Example 2: Creates an authorization rule by providing the primary key</span></span>
```
PS C:\> New-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Manage", "Listen", "Send") -EntityName MyEntity -EntityType Queue -PrimaryKey P+lL/Mnd2Z9sj5hwMrRyAxQDdX8RHfbdqU2eIAqs1rc=
```

<span data-ttu-id="c478b-113">Crea una nuova regola di autorizzazione nel livello di coda di entità con tutte le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="c478b-113">Creates new authorization rule on MyEntity Queue level with all permissions.</span></span>

## <span data-ttu-id="c478b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c478b-114">PARAMETERS</span></span>

### <span data-ttu-id="c478b-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="c478b-115">-EntityName</span></span>
<span data-ttu-id="c478b-116">Specifica il nome dell'entità a cui applicare la regola.</span><span class="sxs-lookup"><span data-stu-id="c478b-116">Specifies the entity name to apply rule at.</span></span>

```yaml
Type: String
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c478b-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="c478b-117">-EntityType</span></span>
<span data-ttu-id="c478b-118">Specifica il tipo di entità.</span><span class="sxs-lookup"><span data-stu-id="c478b-118">Specifies the entity type.</span></span>
<span data-ttu-id="c478b-119">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="c478b-119">Valid values are:</span></span>
  
- <span data-ttu-id="c478b-120">Coda</span><span class="sxs-lookup"><span data-stu-id="c478b-120">Queue</span></span>
- <span data-ttu-id="c478b-121">Argomento</span><span class="sxs-lookup"><span data-stu-id="c478b-121">Topic</span></span>
- <span data-ttu-id="c478b-122">Inoltro</span><span class="sxs-lookup"><span data-stu-id="c478b-122">Relay</span></span>
- <span data-ttu-id="c478b-123">NotificationHub</span><span class="sxs-lookup"><span data-stu-id="c478b-123">NotificationHub</span></span>

```yaml
Type: ServiceBusEntityType
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c478b-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="c478b-124">-Name</span></span>
<span data-ttu-id="c478b-125">Specifica il nome della regola di autorizzazione univoco.</span><span class="sxs-lookup"><span data-stu-id="c478b-125">Specifies the unique authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c478b-126">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c478b-126">-Namespace</span></span>
<span data-ttu-id="c478b-127">Specifica il nome dello spazio dei nomi per applicare la regola di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="c478b-127">Specifies the namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="c478b-128">Se nessun *EntityName* ha specificato che la regola sarà sul livello dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="c478b-128">If no *EntityName* provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="c478b-129">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="c478b-129">-Permission</span></span>
<span data-ttu-id="c478b-130">Autorizzazioni di autorizzazione (Invia, Gestisci, ascolta).</span><span class="sxs-lookup"><span data-stu-id="c478b-130">The authorization permissions (Send, Manage, Listen).</span></span>

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

### <span data-ttu-id="c478b-131">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="c478b-131">-PrimaryKey</span></span>
<span data-ttu-id="c478b-132">Specifica la chiave primaria della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="c478b-132">Specifies the Shared Access Signature primary key.</span></span>
<span data-ttu-id="c478b-133">Verrà generato se non specificato.</span><span class="sxs-lookup"><span data-stu-id="c478b-133">Will be generated if not provided.</span></span>

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

### <span data-ttu-id="c478b-134">-Profile</span><span class="sxs-lookup"><span data-stu-id="c478b-134">-Profile</span></span>
<span data-ttu-id="c478b-135">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c478b-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c478b-136">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c478b-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c478b-137">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="c478b-137">-SecondaryKey</span></span>
<span data-ttu-id="c478b-138">Specifica la chiave secondaria della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="c478b-138">Specifies the Shared Access Signature secondary key.</span></span>

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

### <span data-ttu-id="c478b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c478b-139">CommonParameters</span></span>
<span data-ttu-id="c478b-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c478b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c478b-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c478b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c478b-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c478b-142">INPUTS</span></span>

## <span data-ttu-id="c478b-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c478b-143">OUTPUTS</span></span>

## <span data-ttu-id="c478b-144">Note</span><span class="sxs-lookup"><span data-stu-id="c478b-144">NOTES</span></span>

## <span data-ttu-id="c478b-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c478b-145">RELATED LINKS</span></span>

[<span data-ttu-id="c478b-146">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c478b-146">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="c478b-147">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c478b-147">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)

[<span data-ttu-id="c478b-148">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c478b-148">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


