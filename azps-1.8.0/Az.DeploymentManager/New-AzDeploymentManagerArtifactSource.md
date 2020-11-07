---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 09feb94b046ef6a41130c26ae5e7b996ecbd8771
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684462"
---
# <span data-ttu-id="c53cd-101">New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="c53cd-101">New-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="c53cd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c53cd-102">SYNOPSIS</span></span>
<span data-ttu-id="c53cd-103">Crea un'origine di elementi.</span><span class="sxs-lookup"><span data-stu-id="c53cd-103">Creates an artifact source.</span></span>

## <span data-ttu-id="c53cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c53cd-104">SYNTAX</span></span>

```
New-AzDeploymentManagerArtifactSource -ResourceGroupName <String> -Name <String> -Location <String>
 -SasUri <String> [-Tag <Hashtable>] [-ArtifactRoot <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c53cd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c53cd-105">DESCRIPTION</span></span>
<span data-ttu-id="c53cd-106">Il cmdlet **New-AzDeploymentManagerArtifactSource** crea un'origine di elementi.</span><span class="sxs-lookup"><span data-stu-id="c53cd-106">The **New-AzDeploymentManagerArtifactSource** cmdlet creates an artifact source.</span></span>
<span data-ttu-id="c53cd-107">Specificare il *nome* , *ResourceGroupName* e le proprietà obbligatorie.</span><span class="sxs-lookup"><span data-stu-id="c53cd-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="c53cd-108">Puoi modificare l'oggetto restituito localmente e quindi applicare le modifiche all'origine dell'elemento usando il cmdlet Set-AzDeploymentManagerArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="c53cd-108">You can modify the returned object locally and then apply the changes to the artifact source by using the Set-AzDeploymentManagerArtifactSource cmdlet.</span></span>

<span data-ttu-id="c53cd-109">Il cmdlet restituisce un oggetto ArtifactSource con un ResourceId a cui è possibile fare riferimento nel cmdlet New-AzDeloymentManagerServiceTopology in modo che sia possibile fare riferimento a elementi necessari per una risorsa ServiceUnit, il modello e i file di parametri da questa posizione.</span><span class="sxs-lookup"><span data-stu-id="c53cd-109">The cmdlet returns an ArtifactSource object that has a ResourceId which can be referenced in the New-AzDeloymentManagerServiceTopology cmdlet so that artifacts required for a ServiceUnit resource, the Template and Parameters files, can be referenced from this location.</span></span>

## <span data-ttu-id="c53cd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c53cd-110">EXAMPLES</span></span>

### <span data-ttu-id="c53cd-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c53cd-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerArtifactSource -ResourceGroupName ContosoResourceGroup -Name ContosoArtifactSource -Location "Central US" -SasUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts?sasParameters"
```

<span data-ttu-id="c53cd-112">Crea un'origine dell'elemento in ContosoResourceGroup con il nome ContosoArtifactSource con il centro degli Stati Uniti come posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c53cd-112">Creates an artifact source in the ContosoResourceGroup with the name ContosoArtifactSource with Central US as the location of the resource.</span></span> <span data-ttu-id="c53cd-113">La proprietà SasUri fornisce un URI SAS di archiviazione di Azure al contenitore di archiviazione in cui sono archiviati gli elementi.</span><span class="sxs-lookup"><span data-stu-id="c53cd-113">The SasUri property provides an Azure Storage SAS Uri to the storage container where the artifacts are stored.</span></span>

## <span data-ttu-id="c53cd-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c53cd-114">PARAMETERS</span></span>

### <span data-ttu-id="c53cd-115">-ArtifactRoot</span><span class="sxs-lookup"><span data-stu-id="c53cd-115">-ArtifactRoot</span></span>
<span data-ttu-id="c53cd-116">Offset della directory facoltativa sotto il contenitore di archiviazione per gli elementi.</span><span class="sxs-lookup"><span data-stu-id="c53cd-116">The optional directory offset under the storage container for the artifacts.</span></span>

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

### <span data-ttu-id="c53cd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c53cd-117">-DefaultProfile</span></span>
<span data-ttu-id="c53cd-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c53cd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c53cd-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c53cd-119">-Location</span></span>
<span data-ttu-id="c53cd-120">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c53cd-120">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c53cd-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c53cd-121">-Name</span></span>
<span data-ttu-id="c53cd-122">Nome dell'origine dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="c53cd-122">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c53cd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c53cd-123">-ResourceGroupName</span></span>
<span data-ttu-id="c53cd-124">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="c53cd-124">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c53cd-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="c53cd-125">-SasUri</span></span>
<span data-ttu-id="c53cd-126">URI SAS per il contenitore di archiviazione di Azure in cui sono archiviati gli elementi.</span><span class="sxs-lookup"><span data-stu-id="c53cd-126">The SAS Uri to the Azure storage container where the artifacts are stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c53cd-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="c53cd-127">-Tag</span></span>
<span data-ttu-id="c53cd-128">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="c53cd-128">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c53cd-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c53cd-129">-Confirm</span></span>
<span data-ttu-id="c53cd-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c53cd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c53cd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c53cd-131">-WhatIf</span></span>
<span data-ttu-id="c53cd-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c53cd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c53cd-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c53cd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c53cd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c53cd-134">CommonParameters</span></span>
<span data-ttu-id="c53cd-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c53cd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c53cd-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c53cd-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c53cd-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c53cd-137">INPUTS</span></span>

### <span data-ttu-id="c53cd-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c53cd-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c53cd-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c53cd-139">OUTPUTS</span></span>

### <span data-ttu-id="c53cd-140">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="c53cd-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="c53cd-141">Note</span><span class="sxs-lookup"><span data-stu-id="c53cd-141">NOTES</span></span>

## <span data-ttu-id="c53cd-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c53cd-142">RELATED LINKS</span></span>