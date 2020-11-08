---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 91694efaeaf1a24018269706f3ee388feb7218ea
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191318"
---
# <span data-ttu-id="77dd9-101">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="77dd9-101">Get-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="77dd9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="77dd9-102">SYNOPSIS</span></span>
<span data-ttu-id="77dd9-103">Elenca tutti gli arricchimenti dei messaggi o un particolare arricchimento del messaggio per il tuo hub.</span><span class="sxs-lookup"><span data-stu-id="77dd9-103">Lists all message enrichments or a particular message enrichment for your IoT Hub.</span></span>

## <span data-ttu-id="77dd9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77dd9-104">SYNTAX</span></span>

### <span data-ttu-id="77dd9-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="77dd9-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77dd9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="77dd9-106">InputObjectSet</span></span>
```
Get-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77dd9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="77dd9-107">ResourceIdSet</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="77dd9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77dd9-108">DESCRIPTION</span></span>
<span data-ttu-id="77dd9-109">Per una spiegazione dettagliata degli arricchimenti dei messaggi in Azure molto Hub, vedere https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="77dd9-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="77dd9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77dd9-110">EXAMPLES</span></span>

### <span data-ttu-id="77dd9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="77dd9-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub"

Key  Value   Endpoint(s)
---  -----   -----------
key1 value1  {endpoint1, endpoint2}
key2 value2  {endpoint3, endpoint4}
```

<span data-ttu-id="77dd9-112">Elenca tutti gli arricchimenti dei messaggi in MyIotHub</span><span class="sxs-lookup"><span data-stu-id="77dd9-112">List all message enrichments in MyIotHub</span></span>

### <span data-ttu-id="77dd9-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="77dd9-113">Example 2</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey"

Key         : key1
Value       : value1
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="77dd9-114">Visualizzare i dettagli sull'arricchimento dei messaggi di "newKey".</span><span class="sxs-lookup"><span data-stu-id="77dd9-114">Show details about "newKey" message enrichment.</span></span>

## <span data-ttu-id="77dd9-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="77dd9-115">PARAMETERS</span></span>

### <span data-ttu-id="77dd9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77dd9-116">-DefaultProfile</span></span>
<span data-ttu-id="77dd9-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="77dd9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77dd9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77dd9-118">-InputObject</span></span>
<span data-ttu-id="77dd9-119">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="77dd9-119">IotHub object</span></span>

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

### <span data-ttu-id="77dd9-120">-Key</span><span class="sxs-lookup"><span data-stu-id="77dd9-120">-Key</span></span>
<span data-ttu-id="77dd9-121">Chiave di arricchimento.</span><span class="sxs-lookup"><span data-stu-id="77dd9-121">The enrichment's key.</span></span>

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

### <span data-ttu-id="77dd9-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="77dd9-122">-Name</span></span>
<span data-ttu-id="77dd9-123">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="77dd9-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="77dd9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77dd9-124">-ResourceGroupName</span></span>
<span data-ttu-id="77dd9-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="77dd9-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="77dd9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77dd9-126">-ResourceId</span></span>
<span data-ttu-id="77dd9-127">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="77dd9-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="77dd9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77dd9-128">CommonParameters</span></span>
<span data-ttu-id="77dd9-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77dd9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77dd9-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77dd9-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77dd9-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="77dd9-131">INPUTS</span></span>

### <span data-ttu-id="77dd9-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="77dd9-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="77dd9-133">System. String</span><span class="sxs-lookup"><span data-stu-id="77dd9-133">System.String</span></span>

## <span data-ttu-id="77dd9-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77dd9-134">OUTPUTS</span></span>

### <span data-ttu-id="77dd9-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="77dd9-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

### <span data-ttu-id="77dd9-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSEnrichmentProperties []</span><span class="sxs-lookup"><span data-stu-id="77dd9-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span></span>

## <span data-ttu-id="77dd9-137">Note</span><span class="sxs-lookup"><span data-stu-id="77dd9-137">NOTES</span></span>

## <span data-ttu-id="77dd9-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77dd9-138">RELATED LINKS</span></span>
