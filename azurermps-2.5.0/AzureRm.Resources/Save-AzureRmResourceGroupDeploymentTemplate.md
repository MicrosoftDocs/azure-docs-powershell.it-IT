---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/save-azurermresourcegroupdeploymenttemplate
schema: 2.0.0
ms.openlocfilehash: 78ad8ee76aeeec4f57e0d2f2a6b2a1f4d9424d97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866010"
---
# <span data-ttu-id="b4e4b-101">Save-AzureRmResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="b4e4b-101">Save-AzureRmResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="b4e4b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b4e4b-102">SYNOPSIS</span></span>
<span data-ttu-id="b4e4b-103">Salva un modello di distribuzione di un gruppo di risorse in un file.</span><span class="sxs-lookup"><span data-stu-id="b4e4b-103">Saves a resource group deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4e4b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4e4b-104">SYNTAX</span></span>

```
Save-AzureRmResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4e4b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4e4b-105">DESCRIPTION</span></span>
<span data-ttu-id="b4e4b-106">Il cmdlet **Save-AzureRmResourceGroupDeploymentTemplate**  salva un modello di distribuzione di un gruppo di risorse in un file JSON.</span><span class="sxs-lookup"><span data-stu-id="b4e4b-106">The **Save-AzureRmResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="b4e4b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4e4b-107">EXAMPLES</span></span>

### <span data-ttu-id="b4e4b-108">Esempio 1: salvare un modello di distribuzione</span><span class="sxs-lookup"><span data-stu-id="b4e4b-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzureRmResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="b4e4b-109">Questo comando consente di ottenere il modello di distribuzione da TestDeployment e di salvarlo come file JSON nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="b4e4b-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="b4e4b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b4e4b-110">PARAMETERS</span></span>

### <span data-ttu-id="b4e4b-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b4e4b-111">-ApiVersion</span></span>
<span data-ttu-id="b4e4b-112">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="b4e4b-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b4e4b-113">Se non viene specificato, viene usata la versione più recente dell'API.</span><span class="sxs-lookup"><span data-stu-id="b4e4b-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="b4e4b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4e4b-114">-DefaultProfile</span></span>
<span data-ttu-id="b4e4b-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b4e4b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4e4b-116">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="b4e4b-116">-DeploymentName</span></span>
<span data-ttu-id="b4e4b-117">Specifica il nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b4e4b-117">Specifies the name of the deployment.</span></span>

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

### <span data-ttu-id="b4e4b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b4e4b-118">-Force</span></span>
<span data-ttu-id="b4e4b-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b4e4b-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b4e4b-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b4e4b-120">-InformationAction</span></span>
<span data-ttu-id="b4e4b-121">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="b4e4b-121">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="b4e4b-122">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b4e4b-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b4e4b-123">Continuare</span><span class="sxs-lookup"><span data-stu-id="b4e4b-123">Continue</span></span>
- <span data-ttu-id="b4e4b-124">Ignora</span><span class="sxs-lookup"><span data-stu-id="b4e4b-124">Ignore</span></span>
- <span data-ttu-id="b4e4b-125">Informarsi</span><span class="sxs-lookup"><span data-stu-id="b4e4b-125">Inquire</span></span>
- <span data-ttu-id="b4e4b-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b4e4b-126">SilentlyContinue</span></span>
- <span data-ttu-id="b4e4b-127">Stop</span><span class="sxs-lookup"><span data-stu-id="b4e4b-127">Stop</span></span>
- <span data-ttu-id="b4e4b-128">Sospensione</span><span class="sxs-lookup"><span data-stu-id="b4e4b-128">Suspend</span></span>

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

### <span data-ttu-id="b4e4b-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b4e4b-129">-InformationVariable</span></span>
<span data-ttu-id="b4e4b-130">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="b4e4b-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b4e4b-131">-Path</span><span class="sxs-lookup"><span data-stu-id="b4e4b-131">-Path</span></span>
<span data-ttu-id="b4e4b-132">Specifica il percorso di output del file di modello.</span><span class="sxs-lookup"><span data-stu-id="b4e4b-132">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="b4e4b-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="b4e4b-133">-Pre</span></span>
<span data-ttu-id="b4e4b-134">Indica che questo cmdlet USA versioni dell'API di pre-rilascio quando determina automaticamente la versione dell'API da usare.</span><span class="sxs-lookup"><span data-stu-id="b4e4b-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="b4e4b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4e4b-135">-ResourceGroupName</span></span>
<span data-ttu-id="b4e4b-136">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b4e4b-136">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b4e4b-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b4e4b-137">-Confirm</span></span>
<span data-ttu-id="b4e4b-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4e4b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4e4b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4e4b-139">-WhatIf</span></span>
<span data-ttu-id="b4e4b-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4e4b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4e4b-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4e4b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4e4b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4e4b-142">CommonParameters</span></span>
<span data-ttu-id="b4e4b-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4e4b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4e4b-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4e4b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4e4b-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b4e4b-145">INPUTS</span></span>

## <span data-ttu-id="b4e4b-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4e4b-146">OUTPUTS</span></span>

## <span data-ttu-id="b4e4b-147">Note</span><span class="sxs-lookup"><span data-stu-id="b4e4b-147">NOTES</span></span>

## <span data-ttu-id="b4e4b-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4e4b-148">RELATED LINKS</span></span>
