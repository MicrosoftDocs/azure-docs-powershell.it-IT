---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 6cfda34b1718cfd73108362ee81fbe9c638310c7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333715"
---
# <span data-ttu-id="4d6ed-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="4d6ed-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="4d6ed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d6ed-102">SYNOPSIS</span></span>
<span data-ttu-id="4d6ed-103">Ottiene le chiavi per un runtime di integrazione ospitata autonomamente.</span><span class="sxs-lookup"><span data-stu-id="4d6ed-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="4d6ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d6ed-104">SYNTAX</span></span>

### <span data-ttu-id="4d6ed-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4d6ed-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d6ed-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4d6ed-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4d6ed-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="4d6ed-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d6ed-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d6ed-108">DESCRIPTION</span></span>
<span data-ttu-id="4d6ed-109">Ottenere le chiavi per un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="4d6ed-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="4d6ed-110">I tasti vengono usati per registrare un nodo runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="4d6ed-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="4d6ed-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d6ed-111">EXAMPLES</span></span>

### <span data-ttu-id="4d6ed-112">Esempio 1: ottenere chiavi di runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="4d6ed-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="4d6ed-113">Il cmdlet recupera le chiavi per un runtime di integrazione denominato "test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="4d6ed-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="4d6ed-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d6ed-114">PARAMETERS</span></span>

### <span data-ttu-id="4d6ed-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="4d6ed-115">-DataFactoryName</span></span>
<span data-ttu-id="4d6ed-116">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="4d6ed-116">The data factory name.</span></span>

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

### <span data-ttu-id="4d6ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d6ed-117">-DefaultProfile</span></span>
<span data-ttu-id="4d6ed-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d6ed-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d6ed-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d6ed-119">-InputObject</span></span>
<span data-ttu-id="4d6ed-120">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="4d6ed-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="4d6ed-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d6ed-121">-Name</span></span>
<span data-ttu-id="4d6ed-122">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="4d6ed-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="4d6ed-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d6ed-123">-ResourceGroupName</span></span>
<span data-ttu-id="4d6ed-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4d6ed-124">The resource group name.</span></span>

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

### <span data-ttu-id="4d6ed-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d6ed-125">-ResourceId</span></span>
<span data-ttu-id="4d6ed-126">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="4d6ed-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4d6ed-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d6ed-127">CommonParameters</span></span>
<span data-ttu-id="4d6ed-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d6ed-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d6ed-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d6ed-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d6ed-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d6ed-130">INPUTS</span></span>

### <span data-ttu-id="4d6ed-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4d6ed-131">System.String</span></span>

### <span data-ttu-id="4d6ed-132">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4d6ed-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="4d6ed-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d6ed-133">OUTPUTS</span></span>

### <span data-ttu-id="4d6ed-134">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="4d6ed-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="4d6ed-135">Note</span><span class="sxs-lookup"><span data-stu-id="4d6ed-135">NOTES</span></span>

## <span data-ttu-id="4d6ed-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d6ed-136">RELATED LINKS</span></span>

[<span data-ttu-id="4d6ed-137">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="4d6ed-137">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
