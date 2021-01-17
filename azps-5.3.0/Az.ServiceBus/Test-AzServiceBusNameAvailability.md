---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: adaf7485b0af16821a1f4adec7919422bef07f90
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98485951"
---
# <span data-ttu-id="2ec97-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="2ec97-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="2ec97-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ec97-102">SYNOPSIS</span></span>
<span data-ttu-id="2ec97-103">Controlla la disponibilità della coda o del nome dell'argomento indicato</span><span class="sxs-lookup"><span data-stu-id="2ec97-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="2ec97-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ec97-104">SYNTAX</span></span>

### <span data-ttu-id="2ec97-105">QueueCheckNameAvailabilitySet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2ec97-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ec97-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2ec97-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ec97-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ec97-107">DESCRIPTION</span></span>
<span data-ttu-id="2ec97-108">Il cmdlet **test-AzServiceBusNameAvailability** verifica la disponibilità del nome fornito della coda o dell'argomento</span><span class="sxs-lookup"><span data-stu-id="2ec97-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="2ec97-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ec97-109">EXAMPLES</span></span>

### <span data-ttu-id="2ec97-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2ec97-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="2ec97-111">Restituisce vero se il nome $nameQueue specificato è availabile o restituisce false se specificato $nameQueue nome in non disponibile</span><span class="sxs-lookup"><span data-stu-id="2ec97-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="2ec97-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2ec97-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="2ec97-113">Restituisce vero se il nome $nameTopic specificato è availabile o restituisce false se specificato $nameTopic nome in non disponibile</span><span class="sxs-lookup"><span data-stu-id="2ec97-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="2ec97-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ec97-114">PARAMETERS</span></span>

### <span data-ttu-id="2ec97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ec97-115">-DefaultProfile</span></span>
<span data-ttu-id="2ec97-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ec97-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ec97-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="2ec97-117">-Name</span></span>
<span data-ttu-id="2ec97-118">Nome coda per verificare la disponibilità dei nomi</span><span class="sxs-lookup"><span data-stu-id="2ec97-118">Queue Name to check the Name Availability</span></span>

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

### <span data-ttu-id="2ec97-119">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2ec97-119">-Namespace</span></span>
<span data-ttu-id="2ec97-120">Nome dello spazio dei nomi ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2ec97-120">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="2ec97-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="2ec97-121">-Queue</span></span>
<span data-ttu-id="2ec97-122">Per controllare la disponibilità dei nomi per il nome della coda</span><span class="sxs-lookup"><span data-stu-id="2ec97-122">To Check Name Availability for Queue Name</span></span>

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

### <span data-ttu-id="2ec97-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ec97-123">-ResourceGroupName</span></span>
<span data-ttu-id="2ec97-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="2ec97-124">Resource Group Name</span></span>

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

### <span data-ttu-id="2ec97-125">-Topic</span><span class="sxs-lookup"><span data-stu-id="2ec97-125">-Topic</span></span>
<span data-ttu-id="2ec97-126">Per controllare la disponibilità dei nomi per il nome dell'argomento</span><span class="sxs-lookup"><span data-stu-id="2ec97-126">To Check Name Availability for Topic Name</span></span>

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

### <span data-ttu-id="2ec97-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ec97-127">CommonParameters</span></span>
<span data-ttu-id="2ec97-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ec97-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2ec97-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ec97-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ec97-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ec97-130">INPUTS</span></span>

### <span data-ttu-id="2ec97-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2ec97-131">System.String</span></span>

## <span data-ttu-id="2ec97-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ec97-132">OUTPUTS</span></span>

### <span data-ttu-id="2ec97-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2ec97-133">System.Boolean</span></span>

## <span data-ttu-id="2ec97-134">Note</span><span class="sxs-lookup"><span data-stu-id="2ec97-134">NOTES</span></span>

## <span data-ttu-id="2ec97-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ec97-135">RELATED LINKS</span></span>
