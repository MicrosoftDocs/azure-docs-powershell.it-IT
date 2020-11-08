---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 6cfda34b1718cfd73108362ee81fbe9c638310c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94193008"
---
# <span data-ttu-id="8b612-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="8b612-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="8b612-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8b612-102">SYNOPSIS</span></span>
<span data-ttu-id="8b612-103">Ottiene le chiavi per un runtime di integrazione ospitata autonomamente.</span><span class="sxs-lookup"><span data-stu-id="8b612-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="8b612-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b612-104">SYNTAX</span></span>

### <span data-ttu-id="8b612-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8b612-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b612-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8b612-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b612-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="8b612-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b612-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b612-108">DESCRIPTION</span></span>
<span data-ttu-id="8b612-109">Ottenere le chiavi per un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="8b612-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="8b612-110">I tasti vengono usati per registrare un nodo runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="8b612-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="8b612-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b612-111">EXAMPLES</span></span>

### <span data-ttu-id="8b612-112">Esempio 1: ottenere chiavi di runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="8b612-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="8b612-113">Il cmdlet recupera le chiavi per un runtime di integrazione denominato "test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="8b612-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="8b612-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8b612-114">PARAMETERS</span></span>

### <span data-ttu-id="8b612-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="8b612-115">-DataFactoryName</span></span>
<span data-ttu-id="8b612-116">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="8b612-116">The data factory name.</span></span>

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

### <span data-ttu-id="8b612-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b612-117">-DefaultProfile</span></span>
<span data-ttu-id="8b612-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b612-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b612-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b612-119">-InputObject</span></span>
<span data-ttu-id="8b612-120">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="8b612-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="8b612-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b612-121">-Name</span></span>
<span data-ttu-id="8b612-122">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="8b612-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="8b612-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b612-123">-ResourceGroupName</span></span>
<span data-ttu-id="8b612-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8b612-124">The resource group name.</span></span>

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

### <span data-ttu-id="8b612-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b612-125">-ResourceId</span></span>
<span data-ttu-id="8b612-126">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="8b612-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8b612-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b612-127">CommonParameters</span></span>
<span data-ttu-id="8b612-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b612-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b612-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b612-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b612-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8b612-130">INPUTS</span></span>

### <span data-ttu-id="8b612-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8b612-131">System.String</span></span>

### <span data-ttu-id="8b612-132">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8b612-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="8b612-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b612-133">OUTPUTS</span></span>

### <span data-ttu-id="8b612-134">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="8b612-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="8b612-135">Note</span><span class="sxs-lookup"><span data-stu-id="8b612-135">NOTES</span></span>

## <span data-ttu-id="8b612-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b612-136">RELATED LINKS</span></span>

[<span data-ttu-id="8b612-137">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="8b612-137">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()