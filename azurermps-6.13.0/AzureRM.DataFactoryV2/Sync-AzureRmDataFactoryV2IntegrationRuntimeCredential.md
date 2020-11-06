---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/sync-azurermdatafactoryv2integrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: 05b9c5bce3158413f562c38eb116523609696523
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515395"
---
# <span data-ttu-id="85b31-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="85b31-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="85b31-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85b31-102">SYNOPSIS</span></span>
<span data-ttu-id="85b31-103">Sincronizza le credenziali tra i nodi di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="85b31-103">Synchronizes credentials among integration runtime nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85b31-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85b31-104">SYNTAX</span></span>

### <span data-ttu-id="85b31-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="85b31-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85b31-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="85b31-106">ByResourceId</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85b31-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="85b31-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85b31-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85b31-108">DESCRIPTION</span></span>
<span data-ttu-id="85b31-109">Il cmdlet **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** sincronizza le credenziali locali tra i nodi di Integration Runtime, che obbligano le credenziali a essere identiche in tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="85b31-109">The **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="85b31-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85b31-110">EXAMPLES</span></span>

### <span data-ttu-id="85b31-111">Esempio 1: sincronizzare una credenziale di Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="85b31-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="85b31-112">Il cmdlet sincronizza le credenziali tra i nodi di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="85b31-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="85b31-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85b31-113">PARAMETERS</span></span>

### <span data-ttu-id="85b31-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="85b31-114">-DataFactoryName</span></span>
<span data-ttu-id="85b31-115">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="85b31-115">The data factory name.</span></span>

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

### <span data-ttu-id="85b31-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85b31-116">-DefaultProfile</span></span>
<span data-ttu-id="85b31-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85b31-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85b31-118">-Force</span><span class="sxs-lookup"><span data-stu-id="85b31-118">-Force</span></span>
<span data-ttu-id="85b31-119">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="85b31-119">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85b31-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85b31-120">-InputObject</span></span>
<span data-ttu-id="85b31-121">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="85b31-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="85b31-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="85b31-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="85b31-123">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="85b31-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85b31-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85b31-124">-ResourceGroupName</span></span>
<span data-ttu-id="85b31-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="85b31-125">The resource group name.</span></span>

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

### <span data-ttu-id="85b31-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85b31-126">-ResourceId</span></span>
<span data-ttu-id="85b31-127">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="85b31-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="85b31-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="85b31-128">-Confirm</span></span>
<span data-ttu-id="85b31-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85b31-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85b31-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85b31-130">-WhatIf</span></span>
<span data-ttu-id="85b31-131">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85b31-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85b31-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85b31-132">CommonParameters</span></span>
<span data-ttu-id="85b31-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85b31-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85b31-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85b31-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85b31-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85b31-135">INPUTS</span></span>

### <span data-ttu-id="85b31-136">System. String</span><span class="sxs-lookup"><span data-stu-id="85b31-136">System.String</span></span>

### <span data-ttu-id="85b31-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="85b31-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="85b31-138">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="85b31-138">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="85b31-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85b31-139">OUTPUTS</span></span>

### <span data-ttu-id="85b31-140">System. void</span><span class="sxs-lookup"><span data-stu-id="85b31-140">System.Void</span></span>

## <span data-ttu-id="85b31-141">Note</span><span class="sxs-lookup"><span data-stu-id="85b31-141">NOTES</span></span>

## <span data-ttu-id="85b31-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85b31-142">RELATED LINKS</span></span>
