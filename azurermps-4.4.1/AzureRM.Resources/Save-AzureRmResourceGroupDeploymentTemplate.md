---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 8f146c6516226c800f45489e1f7fa5d37173e151
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688242"
---
# <span data-ttu-id="c3cbc-101">Save-AzureRmResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="c3cbc-101">Save-AzureRmResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="c3cbc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3cbc-102">SYNOPSIS</span></span>
<span data-ttu-id="c3cbc-103">Salva un modello di distribuzione di un gruppo di risorse in un file.</span><span class="sxs-lookup"><span data-stu-id="c3cbc-103">Saves a resource group deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3cbc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3cbc-104">SYNTAX</span></span>

```
Save-AzureRmResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c3cbc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3cbc-105">DESCRIPTION</span></span>
<span data-ttu-id="c3cbc-106">Il cmdlet **Save-AzureRmResourceGroupDeploymentTemplate**  salva un modello di distribuzione di un gruppo di risorse in un file JSON.</span><span class="sxs-lookup"><span data-stu-id="c3cbc-106">The **Save-AzureRmResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="c3cbc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3cbc-107">EXAMPLES</span></span>

### <span data-ttu-id="c3cbc-108">Esempio 1: salvare un modello di distribuzione</span><span class="sxs-lookup"><span data-stu-id="c3cbc-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzureRmResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="c3cbc-109">Questo comando consente di ottenere il modello di distribuzione da TestDeployment e di salvarlo come file JSON nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="c3cbc-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="c3cbc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3cbc-110">PARAMETERS</span></span>

### <span data-ttu-id="c3cbc-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c3cbc-111">-ApiVersion</span></span>
<span data-ttu-id="c3cbc-112">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="c3cbc-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c3cbc-113">Se non viene specificato, viene usata la versione più recente dell'API.</span><span class="sxs-lookup"><span data-stu-id="c3cbc-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="c3cbc-114">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="c3cbc-114">-DeploymentName</span></span>
<span data-ttu-id="c3cbc-115">Specifica il nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c3cbc-115">Specifies the name of the deployment.</span></span>

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

### <span data-ttu-id="c3cbc-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c3cbc-116">-Force</span></span>
<span data-ttu-id="c3cbc-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c3cbc-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c3cbc-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c3cbc-118">-InformationAction</span></span>
<span data-ttu-id="c3cbc-119">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="c3cbc-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c3cbc-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c3cbc-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c3cbc-121">Continuare</span><span class="sxs-lookup"><span data-stu-id="c3cbc-121">Continue</span></span>
- <span data-ttu-id="c3cbc-122">Ignora</span><span class="sxs-lookup"><span data-stu-id="c3cbc-122">Ignore</span></span>
- <span data-ttu-id="c3cbc-123">Informarsi</span><span class="sxs-lookup"><span data-stu-id="c3cbc-123">Inquire</span></span>
- <span data-ttu-id="c3cbc-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c3cbc-124">SilentlyContinue</span></span>
- <span data-ttu-id="c3cbc-125">Stop</span><span class="sxs-lookup"><span data-stu-id="c3cbc-125">Stop</span></span>
- <span data-ttu-id="c3cbc-126">Sospensione</span><span class="sxs-lookup"><span data-stu-id="c3cbc-126">Suspend</span></span>

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

### <span data-ttu-id="c3cbc-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c3cbc-127">-InformationVariable</span></span>
<span data-ttu-id="c3cbc-128">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="c3cbc-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c3cbc-129">-Path</span><span class="sxs-lookup"><span data-stu-id="c3cbc-129">-Path</span></span>
<span data-ttu-id="c3cbc-130">Specifica il percorso di output del file di modello.</span><span class="sxs-lookup"><span data-stu-id="c3cbc-130">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="c3cbc-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="c3cbc-131">-Pre</span></span>
<span data-ttu-id="c3cbc-132">Indica che questo cmdlet USA versioni dell'API di pre-rilascio quando determina automaticamente la versione dell'API da usare.</span><span class="sxs-lookup"><span data-stu-id="c3cbc-132">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="c3cbc-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3cbc-133">-ResourceGroupName</span></span>
<span data-ttu-id="c3cbc-134">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c3cbc-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c3cbc-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c3cbc-135">-Confirm</span></span>
<span data-ttu-id="c3cbc-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3cbc-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3cbc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3cbc-137">-WhatIf</span></span>
<span data-ttu-id="c3cbc-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3cbc-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3cbc-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3cbc-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3cbc-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3cbc-140">-DefaultProfile</span></span>
<span data-ttu-id="c3cbc-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c3cbc-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3cbc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3cbc-142">CommonParameters</span></span>
<span data-ttu-id="c3cbc-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3cbc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3cbc-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3cbc-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3cbc-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3cbc-145">INPUTS</span></span>

## <span data-ttu-id="c3cbc-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3cbc-146">OUTPUTS</span></span>

### <span data-ttu-id="c3cbc-147">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c3cbc-147">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c3cbc-148">Note</span><span class="sxs-lookup"><span data-stu-id="c3cbc-148">NOTES</span></span>

## <span data-ttu-id="c3cbc-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3cbc-149">RELATED LINKS</span></span>

