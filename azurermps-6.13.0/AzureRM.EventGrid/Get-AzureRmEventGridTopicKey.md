---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 8bd28b3bbe043663a451b235abf46c3a42e235e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688124"
---
# <span data-ttu-id="ffc65-101">Get-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="ffc65-101">Get-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="ffc65-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ffc65-102">SYNOPSIS</span></span>
<span data-ttu-id="ffc65-103">Ottiene i tasti di scelta condivisi usati per pubblicare gli eventi in un argomento della griglia degli eventi.</span><span class="sxs-lookup"><span data-stu-id="ffc65-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffc65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ffc65-104">SYNTAX</span></span>

### <span data-ttu-id="ffc65-105">TopicNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ffc65-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffc65-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffc65-106">TopicInputObjectParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ffc65-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffc65-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ffc65-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ffc65-108">DESCRIPTION</span></span>
<span data-ttu-id="ffc65-109">Ottiene i tasti di scelta condivisi usati per pubblicare gli eventi in un argomento della griglia degli eventi.</span><span class="sxs-lookup"><span data-stu-id="ffc65-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="ffc65-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ffc65-110">EXAMPLES</span></span>

### <span data-ttu-id="ffc65-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ffc65-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="ffc65-112">Ottiene i tasti di scelta condivisi dell'argomento griglia dell'evento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ffc65-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ffc65-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ffc65-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzureRmEventGridTopicKey
```

<span data-ttu-id="ffc65-114">Ottiene i tasti di scelta condivisi dell'argomento griglia dell'evento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ffc65-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="ffc65-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ffc65-115">PARAMETERS</span></span>

### <span data-ttu-id="ffc65-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffc65-116">-DefaultProfile</span></span>
<span data-ttu-id="ffc65-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ffc65-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffc65-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ffc65-118">-InputObject</span></span>
<span data-ttu-id="ffc65-119">Oggetto argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="ffc65-119">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffc65-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ffc65-120">-Name</span></span>
<span data-ttu-id="ffc65-121">Nome argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="ffc65-121">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffc65-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffc65-122">-ResourceGroupName</span></span>
<span data-ttu-id="ffc65-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ffc65-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffc65-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ffc65-124">-ResourceId</span></span>
<span data-ttu-id="ffc65-125">Identificatore delle risorse che rappresenta l'argomento della griglia dell'evento.</span><span class="sxs-lookup"><span data-stu-id="ffc65-125">Resource Identifier representing the Event Grid Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffc65-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffc65-126">CommonParameters</span></span>
<span data-ttu-id="ffc65-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffc65-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffc65-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffc65-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffc65-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ffc65-129">INPUTS</span></span>

### <span data-ttu-id="ffc65-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ffc65-130">System.String</span></span>

### <span data-ttu-id="ffc65-131">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="ffc65-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="ffc65-132">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ffc65-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ffc65-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ffc65-133">OUTPUTS</span></span>

### <span data-ttu-id="ffc65-134">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="ffc65-134">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="ffc65-135">Note</span><span class="sxs-lookup"><span data-stu-id="ffc65-135">NOTES</span></span>

## <span data-ttu-id="ffc65-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ffc65-136">RELATED LINKS</span></span>
