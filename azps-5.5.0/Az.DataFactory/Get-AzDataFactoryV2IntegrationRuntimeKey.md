---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 6cfda34b1718cfd73108362ee81fbe9c638310c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204450"
---
# <span data-ttu-id="787a0-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="787a0-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="787a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="787a0-102">SYNOPSIS</span></span>
<span data-ttu-id="787a0-103">Ottiene le chiavi per un runtime di integrazione self-hosted.</span><span class="sxs-lookup"><span data-stu-id="787a0-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="787a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="787a0-104">SYNTAX</span></span>

### <span data-ttu-id="787a0-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="787a0-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="787a0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="787a0-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="787a0-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="787a0-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="787a0-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="787a0-108">DESCRIPTION</span></span>
<span data-ttu-id="787a0-109">Ottenere le chiavi per un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="787a0-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="787a0-110">Le chiavi vengono usate per registrare un nodo di runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="787a0-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="787a0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="787a0-111">EXAMPLES</span></span>

### <span data-ttu-id="787a0-112">Esempio 1: Ottenere chiavi di runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="787a0-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="787a0-113">Il cmdlet recupera le chiavi per un runtime di integrazione denominato "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="787a0-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="787a0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="787a0-114">PARAMETERS</span></span>

### <span data-ttu-id="787a0-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="787a0-115">-DataFactoryName</span></span>
<span data-ttu-id="787a0-116">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="787a0-116">The data factory name.</span></span>

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

### <span data-ttu-id="787a0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="787a0-117">-DefaultProfile</span></span>
<span data-ttu-id="787a0-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="787a0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="787a0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="787a0-119">-InputObject</span></span>
<span data-ttu-id="787a0-120">Oggetto runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="787a0-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="787a0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="787a0-121">-Name</span></span>
<span data-ttu-id="787a0-122">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="787a0-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="787a0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="787a0-123">-ResourceGroupName</span></span>
<span data-ttu-id="787a0-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="787a0-124">The resource group name.</span></span>

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

### <span data-ttu-id="787a0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="787a0-125">-ResourceId</span></span>
<span data-ttu-id="787a0-126">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="787a0-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="787a0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="787a0-127">CommonParameters</span></span>
<span data-ttu-id="787a0-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="787a0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="787a0-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="787a0-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="787a0-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="787a0-130">INPUTS</span></span>

### <span data-ttu-id="787a0-131">System.String</span><span class="sxs-lookup"><span data-stu-id="787a0-131">System.String</span></span>

### <span data-ttu-id="787a0-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="787a0-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="787a0-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="787a0-133">OUTPUTS</span></span>

### <span data-ttu-id="787a0-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="787a0-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="787a0-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="787a0-135">NOTES</span></span>

## <span data-ttu-id="787a0-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="787a0-136">RELATED LINKS</span></span>

[<span data-ttu-id="787a0-137">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="787a0-137">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
