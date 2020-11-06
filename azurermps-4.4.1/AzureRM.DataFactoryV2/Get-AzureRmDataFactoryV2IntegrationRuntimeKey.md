---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 42ccd34e299439d3288a8a587ce9d62abe198847
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521711"
---
# <span data-ttu-id="6c65b-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="6c65b-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="6c65b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6c65b-102">SYNOPSIS</span></span>
<span data-ttu-id="6c65b-103">Ottiene le chiavi per un runtime di integrazione ospitata autonomamente.</span><span class="sxs-lookup"><span data-stu-id="6c65b-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c65b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c65b-104">SYNTAX</span></span>

### <span data-ttu-id="6c65b-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6c65b-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="6c65b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6c65b-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String>
```

### <span data-ttu-id="6c65b-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="6c65b-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="6c65b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c65b-108">DESCRIPTION</span></span>
<span data-ttu-id="6c65b-109">Ottenere le chiavi per un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="6c65b-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="6c65b-110">I tasti vengono usati per registrare un nodo runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="6c65b-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="6c65b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c65b-111">EXAMPLES</span></span>

### <span data-ttu-id="6c65b-112">Esempio 1: ottenere chiavi di runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="6c65b-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="6c65b-113">Il cmdlet recupera le chiavi per un runtime di integrazione denominato "test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="6c65b-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="6c65b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6c65b-114">PARAMETERS</span></span>

### <span data-ttu-id="6c65b-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="6c65b-115">-DataFactoryName</span></span>
<span data-ttu-id="6c65b-116">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="6c65b-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c65b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c65b-117">-InputObject</span></span>
<span data-ttu-id="6c65b-118">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="6c65b-118">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c65b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c65b-119">-Name</span></span>
<span data-ttu-id="6c65b-120">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="6c65b-120">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c65b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c65b-121">-ResourceGroupName</span></span>
<span data-ttu-id="6c65b-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6c65b-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c65b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c65b-123">-ResourceId</span></span>
<span data-ttu-id="6c65b-124">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="6c65b-124">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="6c65b-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6c65b-125">INPUTS</span></span>

### <span data-ttu-id="6c65b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6c65b-126">System.String</span></span>
<span data-ttu-id="6c65b-127">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6c65b-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span> 


## <span data-ttu-id="6c65b-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c65b-128">OUTPUTS</span></span>

### <span data-ttu-id="6c65b-129">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="6c65b-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>


## <span data-ttu-id="6c65b-130">Note</span><span class="sxs-lookup"><span data-stu-id="6c65b-130">NOTES</span></span>

## <span data-ttu-id="6c65b-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c65b-131">RELATED LINKS</span></span>
[<span data-ttu-id="6c65b-132">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="6c65b-132">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
