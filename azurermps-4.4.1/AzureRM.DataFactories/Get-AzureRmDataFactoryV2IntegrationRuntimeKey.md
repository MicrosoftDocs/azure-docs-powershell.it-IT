---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 7bab6fb42e5d50cc0ede06a42540cf628a5ee4a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520783"
---
# <span data-ttu-id="09f24-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="09f24-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="09f24-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="09f24-102">SYNOPSIS</span></span>
<span data-ttu-id="09f24-103">Ottiene le chiavi per un runtime di integrazione ospitata autonomamente.</span><span class="sxs-lookup"><span data-stu-id="09f24-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09f24-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09f24-104">SYNTAX</span></span>

### <span data-ttu-id="09f24-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="09f24-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09f24-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="09f24-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="09f24-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="09f24-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09f24-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09f24-108">DESCRIPTION</span></span>
<span data-ttu-id="09f24-109">Ottenere le chiavi per un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="09f24-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="09f24-110">I tasti vengono usati per registrare un nodo runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="09f24-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="09f24-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09f24-111">EXAMPLES</span></span>

### <span data-ttu-id="09f24-112">Esempio 1: ottenere chiavi di runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="09f24-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="09f24-113">Il cmdlet recupera le chiavi per un runtime di integrazione denominato "test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="09f24-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="09f24-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="09f24-114">PARAMETERS</span></span>

### <span data-ttu-id="09f24-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="09f24-115">-DataFactoryName</span></span>
<span data-ttu-id="09f24-116">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="09f24-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09f24-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09f24-117">-InputObject</span></span>
<span data-ttu-id="09f24-118">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="09f24-118">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09f24-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="09f24-119">-Name</span></span>
<span data-ttu-id="09f24-120">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="09f24-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09f24-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09f24-121">-ResourceGroupName</span></span>
<span data-ttu-id="09f24-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="09f24-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09f24-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09f24-123">-ResourceId</span></span>
<span data-ttu-id="09f24-124">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="09f24-124">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09f24-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09f24-125">-DefaultProfile</span></span>
<span data-ttu-id="09f24-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="09f24-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09f24-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09f24-127">CommonParameters</span></span>
<span data-ttu-id="09f24-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09f24-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09f24-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09f24-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09f24-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="09f24-130">INPUTS</span></span>

### <span data-ttu-id="09f24-131">System. String</span><span class="sxs-lookup"><span data-stu-id="09f24-131">System.String</span></span>
<span data-ttu-id="09f24-132">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="09f24-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span> 

## <span data-ttu-id="09f24-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09f24-133">OUTPUTS</span></span>

### <span data-ttu-id="09f24-134">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="09f24-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="09f24-135">Note</span><span class="sxs-lookup"><span data-stu-id="09f24-135">NOTES</span></span>

## <span data-ttu-id="09f24-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09f24-136">RELATED LINKS</span></span>

[<span data-ttu-id="09f24-137">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="09f24-137">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
