---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 18a6d5db9ecf7cf02604a883b49545650413ee28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987964"
---
# <span data-ttu-id="b95fa-101">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b95fa-101">Get-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="b95fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b95fa-102">SYNOPSIS</span></span>
<span data-ttu-id="b95fa-103">Elenca tutti gli arricchimenti dei messaggi o un particolare arricchimento dei messaggi per l'Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="b95fa-103">Lists all message enrichments or a particular message enrichment for your IoT Hub.</span></span>

## <span data-ttu-id="b95fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b95fa-104">SYNTAX</span></span>

### <span data-ttu-id="b95fa-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b95fa-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b95fa-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b95fa-106">InputObjectSet</span></span>
```
Get-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b95fa-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b95fa-107">ResourceIdSet</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b95fa-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b95fa-108">DESCRIPTION</span></span>
<span data-ttu-id="b95fa-109">Per una spiegazione dettagliata dell'arricchimento dei messaggi nell'Hub IoT di Azure, vedi https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="b95fa-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="b95fa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b95fa-110">EXAMPLES</span></span>

### <span data-ttu-id="b95fa-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b95fa-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub"

Key  Value   Endpoint(s)
---  -----   -----------
key1 value1  {endpoint1, endpoint2}
key2 value2  {endpoint3, endpoint4}
```

<span data-ttu-id="b95fa-112">Elencare tutti gli arricchimenti dei messaggi in MyIotHub</span><span class="sxs-lookup"><span data-stu-id="b95fa-112">List all message enrichments in MyIotHub</span></span>

### <span data-ttu-id="b95fa-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b95fa-113">Example 2</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey"

Key         : key1
Value       : value1
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="b95fa-114">Visualizzare i dettagli sull'arricchimento del messaggio "newKey".</span><span class="sxs-lookup"><span data-stu-id="b95fa-114">Show details about "newKey" message enrichment.</span></span>

## <span data-ttu-id="b95fa-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b95fa-115">PARAMETERS</span></span>

### <span data-ttu-id="b95fa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b95fa-116">-DefaultProfile</span></span>
<span data-ttu-id="b95fa-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b95fa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b95fa-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b95fa-118">-InputObject</span></span>
<span data-ttu-id="b95fa-119">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="b95fa-119">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b95fa-120">-Key</span><span class="sxs-lookup"><span data-stu-id="b95fa-120">-Key</span></span>
<span data-ttu-id="b95fa-121">Chiave dell'arricchimento.</span><span class="sxs-lookup"><span data-stu-id="b95fa-121">The enrichment's key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95fa-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b95fa-122">-Name</span></span>
<span data-ttu-id="b95fa-123">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="b95fa-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95fa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b95fa-124">-ResourceGroupName</span></span>
<span data-ttu-id="b95fa-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b95fa-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95fa-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b95fa-126">-ResourceId</span></span>
<span data-ttu-id="b95fa-127">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="b95fa-127">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b95fa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b95fa-128">CommonParameters</span></span>
<span data-ttu-id="b95fa-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b95fa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b95fa-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b95fa-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b95fa-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="b95fa-131">INPUTS</span></span>

### <span data-ttu-id="b95fa-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b95fa-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b95fa-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b95fa-133">System.String</span></span>

## <span data-ttu-id="b95fa-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b95fa-134">OUTPUTS</span></span>

### <span data-ttu-id="b95fa-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="b95fa-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

### <span data-ttu-id="b95fa-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span><span class="sxs-lookup"><span data-stu-id="b95fa-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span></span>

## <span data-ttu-id="b95fa-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="b95fa-137">NOTES</span></span>

## <span data-ttu-id="b95fa-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b95fa-138">RELATED LINKS</span></span>
