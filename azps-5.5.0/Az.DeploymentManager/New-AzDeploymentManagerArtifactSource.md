---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: dcd8d4164d091564aef3d3802430ab499eac38ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194535"
---
# <span data-ttu-id="7492b-101">New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="7492b-101">New-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="7492b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7492b-102">SYNOPSIS</span></span>
<span data-ttu-id="7492b-103">Crea un'origine dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="7492b-103">Creates an artifact source.</span></span>

## <span data-ttu-id="7492b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7492b-104">SYNTAX</span></span>

```
New-AzDeploymentManagerArtifactSource -ResourceGroupName <String> -Name <String> -Location <String>
 -SasUri <String> [-Tag <Hashtable>] [-ArtifactRoot <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7492b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7492b-105">DESCRIPTION</span></span>
<span data-ttu-id="7492b-106">Il cmdlet **New-AzDeploymentManagerArtifactSource** crea un'origine dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="7492b-106">The **New-AzDeploymentManagerArtifactSource** cmdlet creates an artifact source.</span></span>
<span data-ttu-id="7492b-107">Specificare le *proprietà Name,* *ResourceGroupName* e required.</span><span class="sxs-lookup"><span data-stu-id="7492b-107">Specify the *Name*, *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="7492b-108">È possibile modificare l'oggetto restituito in locale e quindi applicare le modifiche all'origine dell'elemento usando il cmdlet Set-AzDeploymentManagerArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="7492b-108">You can modify the returned object locally and then apply the changes to the artifact source by using the Set-AzDeploymentManagerArtifactSource cmdlet.</span></span>

<span data-ttu-id="7492b-109">Il cmdlet restituisce un oggetto ArtifactSource con un valore ResourceId a cui è possibile fare riferimento nel cmdlet New-AzDeploymentManagerServiceTopology in modo che da questa posizione sia possibile fare riferimento agli elementi necessari per una risorsa ServiceUnit, i file Template e Parameters.</span><span class="sxs-lookup"><span data-stu-id="7492b-109">The cmdlet returns an ArtifactSource object that has a ResourceId which can be referenced in the New-AzDeploymentManagerServiceTopology cmdlet so that artifacts required for a ServiceUnit resource, the Template and Parameters files, can be referenced from this location.</span></span>

## <span data-ttu-id="7492b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7492b-110">EXAMPLES</span></span>

### <span data-ttu-id="7492b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7492b-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerArtifactSource -ResourceGroupName ContosoResourceGroup -Name ContosoArtifactSource -Location "Central US" -SasUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts?sasParameters"
```

<span data-ttu-id="7492b-112">Crea un'origine dell'elemento in ContosoResourceGroup con il nome ContosoArtifactSource con Stati Uniti centrali come posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7492b-112">Creates an artifact source in the ContosoResourceGroup with the name ContosoArtifactSource with Central US as the location of the resource.</span></span> <span data-ttu-id="7492b-113">La proprietà SasUri fornisce un URI della firma di accesso condiviso di Archiviazione di Azure al contenitore di archiviazione in cui sono archiviati gli elementi.</span><span class="sxs-lookup"><span data-stu-id="7492b-113">The SasUri property provides an Azure Storage SAS Uri to the storage container where the artifacts are stored.</span></span>

## <span data-ttu-id="7492b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7492b-114">PARAMETERS</span></span>

### <span data-ttu-id="7492b-115">-ArtifactRoot</span><span class="sxs-lookup"><span data-stu-id="7492b-115">-ArtifactRoot</span></span>
<span data-ttu-id="7492b-116">Offset della directory facoltativo nel contenitore di archiviazione per gli elementi.</span><span class="sxs-lookup"><span data-stu-id="7492b-116">The optional directory offset under the storage container for the artifacts.</span></span>

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

### <span data-ttu-id="7492b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7492b-117">-DefaultProfile</span></span>
<span data-ttu-id="7492b-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7492b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7492b-119">-Location</span><span class="sxs-lookup"><span data-stu-id="7492b-119">-Location</span></span>
<span data-ttu-id="7492b-120">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7492b-120">The location of the resource.</span></span>

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

### <span data-ttu-id="7492b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7492b-121">-Name</span></span>
<span data-ttu-id="7492b-122">Nome dell'origine dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="7492b-122">The name of the artifact source.</span></span>

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

### <span data-ttu-id="7492b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7492b-123">-ResourceGroupName</span></span>
<span data-ttu-id="7492b-124">Gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7492b-124">The resource group.</span></span>

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

### <span data-ttu-id="7492b-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="7492b-125">-SasUri</span></span>
<span data-ttu-id="7492b-126">Uri della firma di accesso condiviso nel contenitore di archiviazione di Azure in cui sono archiviati gli elementi.</span><span class="sxs-lookup"><span data-stu-id="7492b-126">The SAS Uri to the Azure storage container where the artifacts are stored.</span></span>

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

### <span data-ttu-id="7492b-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="7492b-127">-Tag</span></span>
<span data-ttu-id="7492b-128">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="7492b-128">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="7492b-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7492b-129">-Confirm</span></span>
<span data-ttu-id="7492b-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7492b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7492b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7492b-131">-WhatIf</span></span>
<span data-ttu-id="7492b-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7492b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7492b-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7492b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7492b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7492b-134">CommonParameters</span></span>
<span data-ttu-id="7492b-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7492b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7492b-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7492b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7492b-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="7492b-137">INPUTS</span></span>

### <span data-ttu-id="7492b-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7492b-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7492b-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7492b-139">OUTPUTS</span></span>

### <span data-ttu-id="7492b-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="7492b-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="7492b-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="7492b-141">NOTES</span></span>

## <span data-ttu-id="7492b-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7492b-142">RELATED LINKS</span></span>
