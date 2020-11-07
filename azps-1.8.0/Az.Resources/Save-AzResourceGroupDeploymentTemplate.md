---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azresourcegroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
ms.openlocfilehash: f9532ebaffaaae6a1429cb7ce8680283572c1775
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677277"
---
# <span data-ttu-id="adcfe-101">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="adcfe-101">Save-AzResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="adcfe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="adcfe-102">SYNOPSIS</span></span>
<span data-ttu-id="adcfe-103">Salva un modello di distribuzione di un gruppo di risorse in un file.</span><span class="sxs-lookup"><span data-stu-id="adcfe-103">Saves a resource group deployment template to a file.</span></span>

## <span data-ttu-id="adcfe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="adcfe-104">SYNTAX</span></span>

```
Save-AzResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="adcfe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="adcfe-105">DESCRIPTION</span></span>
<span data-ttu-id="adcfe-106">Il cmdlet **Save-AzResourceGroupDeploymentTemplate**  salva un modello di distribuzione di un gruppo di risorse in un file JSON.</span><span class="sxs-lookup"><span data-stu-id="adcfe-106">The **Save-AzResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="adcfe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="adcfe-107">EXAMPLES</span></span>

### <span data-ttu-id="adcfe-108">Esempio 1: salvare un modello di distribuzione</span><span class="sxs-lookup"><span data-stu-id="adcfe-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="adcfe-109">Questo comando consente di ottenere il modello di distribuzione da TestDeployment e di salvarlo come file JSON nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="adcfe-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="adcfe-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="adcfe-110">PARAMETERS</span></span>

### <span data-ttu-id="adcfe-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="adcfe-111">-ApiVersion</span></span>
<span data-ttu-id="adcfe-112">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="adcfe-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="adcfe-113">Se non viene specificato, viene usata la versione più recente dell'API.</span><span class="sxs-lookup"><span data-stu-id="adcfe-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="adcfe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adcfe-114">-DefaultProfile</span></span>
<span data-ttu-id="adcfe-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="adcfe-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="adcfe-116">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="adcfe-116">-DeploymentName</span></span>
<span data-ttu-id="adcfe-117">Specifica il nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="adcfe-117">Specifies the name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adcfe-118">-Force</span><span class="sxs-lookup"><span data-stu-id="adcfe-118">-Force</span></span>
<span data-ttu-id="adcfe-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="adcfe-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="adcfe-120">-Path</span><span class="sxs-lookup"><span data-stu-id="adcfe-120">-Path</span></span>
<span data-ttu-id="adcfe-121">Specifica il percorso di output del file di modello.</span><span class="sxs-lookup"><span data-stu-id="adcfe-121">Specifies the output path of the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adcfe-122">-Pre</span><span class="sxs-lookup"><span data-stu-id="adcfe-122">-Pre</span></span>
<span data-ttu-id="adcfe-123">Indica che questo cmdlet USA versioni dell'API di pre-rilascio quando determina automaticamente la versione dell'API da usare.</span><span class="sxs-lookup"><span data-stu-id="adcfe-123">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="adcfe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adcfe-124">-ResourceGroupName</span></span>
<span data-ttu-id="adcfe-125">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="adcfe-125">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adcfe-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="adcfe-126">-Confirm</span></span>
<span data-ttu-id="adcfe-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adcfe-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adcfe-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adcfe-128">-WhatIf</span></span>
<span data-ttu-id="adcfe-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="adcfe-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adcfe-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="adcfe-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adcfe-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adcfe-131">CommonParameters</span></span>
<span data-ttu-id="adcfe-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adcfe-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adcfe-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adcfe-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adcfe-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="adcfe-134">INPUTS</span></span>

### <span data-ttu-id="adcfe-135">System. String</span><span class="sxs-lookup"><span data-stu-id="adcfe-135">System.String</span></span>

## <span data-ttu-id="adcfe-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="adcfe-136">OUTPUTS</span></span>

### <span data-ttu-id="adcfe-137">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="adcfe-137">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="adcfe-138">Note</span><span class="sxs-lookup"><span data-stu-id="adcfe-138">NOTES</span></span>

## <span data-ttu-id="adcfe-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="adcfe-139">RELATED LINKS</span></span>
