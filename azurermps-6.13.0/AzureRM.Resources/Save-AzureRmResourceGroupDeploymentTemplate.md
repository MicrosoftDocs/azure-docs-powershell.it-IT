---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/save-azurermresourcegroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 3f73a7d4192f6e77b66698cd84f65b40bc5505fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687769"
---
# <span data-ttu-id="c4c4d-101">Save-AzureRmResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="c4c4d-101">Save-AzureRmResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="c4c4d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c4c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="c4c4d-103">Salva un modello di distribuzione di un gruppo di risorse in un file.</span><span class="sxs-lookup"><span data-stu-id="c4c4d-103">Saves a resource group deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4c4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4c4d-104">SYNTAX</span></span>

```
Save-AzureRmResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4c4d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4c4d-105">DESCRIPTION</span></span>
<span data-ttu-id="c4c4d-106">Il cmdlet **Save-AzureRmResourceGroupDeploymentTemplate**  salva un modello di distribuzione di un gruppo di risorse in un file JSON.</span><span class="sxs-lookup"><span data-stu-id="c4c4d-106">The **Save-AzureRmResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="c4c4d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4c4d-107">EXAMPLES</span></span>

### <span data-ttu-id="c4c4d-108">Esempio 1: salvare un modello di distribuzione</span><span class="sxs-lookup"><span data-stu-id="c4c4d-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzureRmResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="c4c4d-109">Questo comando consente di ottenere il modello di distribuzione da TestDeployment e di salvarlo come file JSON nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="c4c4d-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="c4c4d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c4c4d-110">PARAMETERS</span></span>

### <span data-ttu-id="c4c4d-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c4c4d-111">-ApiVersion</span></span>
<span data-ttu-id="c4c4d-112">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="c4c4d-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c4c4d-113">Se non viene specificato, viene usata la versione più recente dell'API.</span><span class="sxs-lookup"><span data-stu-id="c4c4d-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="c4c4d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4c4d-114">-DefaultProfile</span></span>
<span data-ttu-id="c4c4d-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c4c4d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4c4d-116">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="c4c4d-116">-DeploymentName</span></span>
<span data-ttu-id="c4c4d-117">Specifica il nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c4c4d-117">Specifies the name of the deployment.</span></span>

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

### <span data-ttu-id="c4c4d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c4c4d-118">-Force</span></span>
<span data-ttu-id="c4c4d-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c4c4d-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c4c4d-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c4c4d-120">-InformationAction</span></span>
<span data-ttu-id="c4c4d-121">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="c4c4d-121">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="c4c4d-122">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c4c4d-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c4c4d-123">Continuare</span><span class="sxs-lookup"><span data-stu-id="c4c4d-123">Continue</span></span>
- <span data-ttu-id="c4c4d-124">Ignora</span><span class="sxs-lookup"><span data-stu-id="c4c4d-124">Ignore</span></span>
- <span data-ttu-id="c4c4d-125">Informarsi</span><span class="sxs-lookup"><span data-stu-id="c4c4d-125">Inquire</span></span>
- <span data-ttu-id="c4c4d-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c4c4d-126">SilentlyContinue</span></span>
- <span data-ttu-id="c4c4d-127">Stop</span><span class="sxs-lookup"><span data-stu-id="c4c4d-127">Stop</span></span>
- <span data-ttu-id="c4c4d-128">Sospensione</span><span class="sxs-lookup"><span data-stu-id="c4c4d-128">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4c4d-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c4c4d-129">-InformationVariable</span></span>
<span data-ttu-id="c4c4d-130">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="c4c4d-130">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4c4d-131">-Path</span><span class="sxs-lookup"><span data-stu-id="c4c4d-131">-Path</span></span>
<span data-ttu-id="c4c4d-132">Specifica il percorso di output del file di modello.</span><span class="sxs-lookup"><span data-stu-id="c4c4d-132">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="c4c4d-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="c4c4d-133">-Pre</span></span>
<span data-ttu-id="c4c4d-134">Indica che questo cmdlet USA versioni dell'API di pre-rilascio quando determina automaticamente la versione dell'API da usare.</span><span class="sxs-lookup"><span data-stu-id="c4c4d-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="c4c4d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4c4d-135">-ResourceGroupName</span></span>
<span data-ttu-id="c4c4d-136">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c4c4d-136">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c4c4d-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c4c4d-137">-Confirm</span></span>
<span data-ttu-id="c4c4d-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4c4d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4c4d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4c4d-139">-WhatIf</span></span>
<span data-ttu-id="c4c4d-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4c4d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4c4d-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4c4d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4c4d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4c4d-142">CommonParameters</span></span>
<span data-ttu-id="c4c4d-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4c4d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4c4d-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4c4d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4c4d-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c4c4d-145">INPUTS</span></span>

## <span data-ttu-id="c4c4d-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4c4d-146">OUTPUTS</span></span>

## <span data-ttu-id="c4c4d-147">Note</span><span class="sxs-lookup"><span data-stu-id="c4c4d-147">NOTES</span></span>

## <span data-ttu-id="c4c4d-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4c4d-148">RELATED LINKS</span></span>
