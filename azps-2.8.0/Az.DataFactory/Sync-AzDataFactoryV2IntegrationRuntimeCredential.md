---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/sync-azdatafactoryv2integrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Sync-AzDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Sync-AzDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: 40f6a6c5f446b23a92a2ca5c5c8c872297b2a81a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674902"
---
# <span data-ttu-id="b0d71-101">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="b0d71-101">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="b0d71-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0d71-102">SYNOPSIS</span></span>
<span data-ttu-id="b0d71-103">Sincronizza le credenziali tra i nodi di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="b0d71-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="b0d71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0d71-104">SYNTAX</span></span>

### <span data-ttu-id="b0d71-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b0d71-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0d71-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b0d71-106">ByResourceId</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0d71-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="b0d71-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0d71-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0d71-108">DESCRIPTION</span></span>
<span data-ttu-id="b0d71-109">Il cmdlet **Sync-AzDataFactoryV2IntegrationRuntimeCredential** sincronizza le credenziali locali tra i nodi di Integration Runtime, che obbligano le credenziali a essere identiche in tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="b0d71-109">The **Sync-AzDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="b0d71-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0d71-110">EXAMPLES</span></span>

### <span data-ttu-id="b0d71-111">Esempio 1: sincronizzare una credenziale di Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="b0d71-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="b0d71-112">Il cmdlet sincronizza le credenziali tra i nodi di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="b0d71-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="b0d71-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0d71-113">PARAMETERS</span></span>

### <span data-ttu-id="b0d71-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="b0d71-114">-DataFactoryName</span></span>
<span data-ttu-id="b0d71-115">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="b0d71-115">The data factory name.</span></span>

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

### <span data-ttu-id="b0d71-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0d71-116">-DefaultProfile</span></span>
<span data-ttu-id="b0d71-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0d71-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0d71-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b0d71-118">-Force</span></span>
<span data-ttu-id="b0d71-119">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="b0d71-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b0d71-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0d71-120">-InputObject</span></span>
<span data-ttu-id="b0d71-121">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="b0d71-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="b0d71-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="b0d71-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="b0d71-123">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b0d71-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="b0d71-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0d71-124">-ResourceGroupName</span></span>
<span data-ttu-id="b0d71-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b0d71-125">The resource group name.</span></span>

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

### <span data-ttu-id="b0d71-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0d71-126">-ResourceId</span></span>
<span data-ttu-id="b0d71-127">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="b0d71-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b0d71-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b0d71-128">-Confirm</span></span>
<span data-ttu-id="b0d71-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0d71-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0d71-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0d71-130">-WhatIf</span></span>
<span data-ttu-id="b0d71-131">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0d71-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b0d71-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0d71-132">CommonParameters</span></span>
<span data-ttu-id="b0d71-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0d71-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0d71-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0d71-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0d71-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0d71-135">INPUTS</span></span>

### <span data-ttu-id="b0d71-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b0d71-136">System.String</span></span>

### <span data-ttu-id="b0d71-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b0d71-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b0d71-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0d71-138">OUTPUTS</span></span>

### <span data-ttu-id="b0d71-139">System. void</span><span class="sxs-lookup"><span data-stu-id="b0d71-139">System.Void</span></span>

## <span data-ttu-id="b0d71-140">Note</span><span class="sxs-lookup"><span data-stu-id="b0d71-140">NOTES</span></span>

## <span data-ttu-id="b0d71-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0d71-141">RELATED LINKS</span></span>
