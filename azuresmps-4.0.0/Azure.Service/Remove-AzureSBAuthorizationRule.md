---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E246C177-EAEE-4D7A-A544-664F47862FC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92d450a10628ea7e85a49962ac262d4dece8e4c8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029593"
---
# <span data-ttu-id="87bb0-101">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="87bb0-101">Remove-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="87bb0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="87bb0-102">SYNOPSIS</span></span>
<span data-ttu-id="87bb0-103">Rimuove la regola di autorizzazione di Service Bus esistente.</span><span class="sxs-lookup"><span data-stu-id="87bb0-103">Removes existing Service Bus authorization rule.</span></span>

## <span data-ttu-id="87bb0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="87bb0-104">SYNTAX</span></span>

### <span data-ttu-id="87bb0-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="87bb0-105">EntitySAS</span></span>
```
Remove-AzureSBAuthorizationRule -Name <String> -Namespace <String> -EntityName <String>
 -EntityType <ServiceBusEntityType> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="87bb0-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="87bb0-106">NamespaceSAS</span></span>
```
Remove-AzureSBAuthorizationRule -Name <String> -Namespace <String> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="87bb0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87bb0-107">DESCRIPTION</span></span>
<span data-ttu-id="87bb0-108">Rimuove la regola di autorizzazione di Service Bus esistente.</span><span class="sxs-lookup"><span data-stu-id="87bb0-108">Removes existing Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="87bb0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="87bb0-109">EXAMPLES</span></span>

### <span data-ttu-id="87bb0-110">Esempio 1: rimuovere la regola di autorizzazione a livello di spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="87bb0-110">Example 1: Remove authorization rule at namespace level</span></span>
```
PS C:\> Remove-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace
```

<span data-ttu-id="87bb0-111">Rimuove la regola di autorizzazione da MyNamespace.</span><span class="sxs-lookup"><span data-stu-id="87bb0-111">Removes authorization rule MyRule from MyNamespace.</span></span>

### <span data-ttu-id="87bb0-112">Esempio 2: rimuovere la regola di autorizzazione per una coda</span><span class="sxs-lookup"><span data-stu-id="87bb0-112">Example 2: Remove authorization rule for a Queue</span></span>
```
PS C:\> Remove-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="87bb0-113">Rimuove la regola di autorizzazione denominata regola per una coda di entità in MyNamespace.</span><span class="sxs-lookup"><span data-stu-id="87bb0-113">Removes authorization rule called MyRule for a MyEntity Queue on MyNamespace.</span></span>

## <span data-ttu-id="87bb0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="87bb0-114">PARAMETERS</span></span>

### <span data-ttu-id="87bb0-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="87bb0-115">-EntityName</span></span>
<span data-ttu-id="87bb0-116">Nome dell'entità a cui applicare la regola.</span><span class="sxs-lookup"><span data-stu-id="87bb0-116">The entity name to apply rule at.</span></span>

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

### <span data-ttu-id="87bb0-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="87bb0-117">-EntityType</span></span>
<span data-ttu-id="87bb0-118">Il tipo di entità (Queue, Topic, Relay, NotificationHub).</span><span class="sxs-lookup"><span data-stu-id="87bb0-118">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

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

### <span data-ttu-id="87bb0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="87bb0-119">-Name</span></span>
<span data-ttu-id="87bb0-120">Nome della regola di autorizzazione univoco.</span><span class="sxs-lookup"><span data-stu-id="87bb0-120">The unique authorization rule name.</span></span>

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

### <span data-ttu-id="87bb0-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="87bb0-121">-Namespace</span></span>
<span data-ttu-id="87bb0-122">Nome dello spazio dei nomi per applicare la regola di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="87bb0-122">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="87bb0-123">Se nessun EntityName ha specificato che la regola sarà sul livello dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="87bb0-123">If no EntityName provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="87bb0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87bb0-124">-PassThru</span></span>
<span data-ttu-id="87bb0-125">Indica che questo cmdlet restituisce un oggetto che rappresenta l'elemento in cui opera.</span><span class="sxs-lookup"><span data-stu-id="87bb0-125">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="87bb0-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="87bb0-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87bb0-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="87bb0-127">-Profile</span></span>
<span data-ttu-id="87bb0-128">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87bb0-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="87bb0-129">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="87bb0-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="87bb0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87bb0-130">CommonParameters</span></span>
<span data-ttu-id="87bb0-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87bb0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87bb0-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87bb0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87bb0-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="87bb0-133">INPUTS</span></span>

## <span data-ttu-id="87bb0-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="87bb0-134">OUTPUTS</span></span>

## <span data-ttu-id="87bb0-135">Note</span><span class="sxs-lookup"><span data-stu-id="87bb0-135">NOTES</span></span>

## <span data-ttu-id="87bb0-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="87bb0-136">RELATED LINKS</span></span>

[<span data-ttu-id="87bb0-137">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="87bb0-137">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="87bb0-138">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="87bb0-138">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="87bb0-139">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="87bb0-139">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


