---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: b97acb269ee38dc937c5deffb0b3e054b0222c4d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961566"
---
# <span data-ttu-id="be36f-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="be36f-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="be36f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be36f-102">SYNOPSIS</span></span>
<span data-ttu-id="be36f-103">Verifica la disponibilità del nome della coda o dell'argomento specificato</span><span class="sxs-lookup"><span data-stu-id="be36f-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="be36f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be36f-104">SYNTAX</span></span>

### <span data-ttu-id="be36f-105">QueueCheckNameAvailabilitySet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="be36f-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be36f-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="be36f-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be36f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="be36f-107">DESCRIPTION</span></span>
<span data-ttu-id="be36f-108">Il **cmdlet Test-AzServiceBusNameAvailability** controlla la disponibilità del nome fornito di Queue o Topic</span><span class="sxs-lookup"><span data-stu-id="be36f-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="be36f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be36f-109">EXAMPLES</span></span>

### <span data-ttu-id="be36f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="be36f-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="be36f-111">Restituisce Vero se il nome $nameQueue fornito è Availabile o restituisce Falso se $nameQueue nome non disponibile</span><span class="sxs-lookup"><span data-stu-id="be36f-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="be36f-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="be36f-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="be36f-113">Restituisce Vero se il nome $nameTopic specificato è Availabile o restituisce Falso se $nameTopic nome non disponibile</span><span class="sxs-lookup"><span data-stu-id="be36f-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="be36f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be36f-114">PARAMETERS</span></span>

### <span data-ttu-id="be36f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be36f-115">-DefaultProfile</span></span>
<span data-ttu-id="be36f-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="be36f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be36f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="be36f-117">-Name</span></span>
<span data-ttu-id="be36f-118">Nome coda per controllare la disponibilità del nome</span><span class="sxs-lookup"><span data-stu-id="be36f-118">Queue Name to check the Name Availability</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be36f-119">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="be36f-119">-Namespace</span></span>
<span data-ttu-id="be36f-120">Nome spazio dei nomi Servicebus</span><span class="sxs-lookup"><span data-stu-id="be36f-120">Servicebus Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be36f-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="be36f-121">-Queue</span></span>
<span data-ttu-id="be36f-122">Per verificare la disponibilità del nome per il nome della coda</span><span class="sxs-lookup"><span data-stu-id="be36f-122">To Check Name Availability for Queue Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: QueueCheckNameAvailabilitySet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be36f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be36f-123">-ResourceGroupName</span></span>
<span data-ttu-id="be36f-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="be36f-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be36f-125">-Topic</span><span class="sxs-lookup"><span data-stu-id="be36f-125">-Topic</span></span>
<span data-ttu-id="be36f-126">Per verificare la disponibilità del nome per il nome dell'argomento</span><span class="sxs-lookup"><span data-stu-id="be36f-126">To Check Name Availability for Topic Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TopicCheckNameAvailabilitySet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be36f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be36f-127">CommonParameters</span></span>
<span data-ttu-id="be36f-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be36f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="be36f-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be36f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be36f-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="be36f-130">INPUTS</span></span>

### <span data-ttu-id="be36f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="be36f-131">System.String</span></span>

## <span data-ttu-id="be36f-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be36f-132">OUTPUTS</span></span>

### <span data-ttu-id="be36f-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="be36f-133">System.Boolean</span></span>

## <span data-ttu-id="be36f-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="be36f-134">NOTES</span></span>

## <span data-ttu-id="be36f-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be36f-135">RELATED LINKS</span></span>
