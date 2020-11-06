---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: 230e443fad4740b6bf9896164f02ae9b382e3ed2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491105"
---
# <span data-ttu-id="f759c-101">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="f759c-101">Set-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="f759c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f759c-102">SYNOPSIS</span></span>
<span data-ttu-id="f759c-103">Aggiorna un'origine dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="f759c-103">Updates an artifact source.</span></span>

## <span data-ttu-id="f759c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f759c-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f759c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f759c-105">DESCRIPTION</span></span>
<span data-ttu-id="f759c-106">Il cmdlet **set-AzureRmDeploymentManagerArtifactSource** aggiorna un'origine dell'elemento con l'oggetto origine dell'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="f759c-106">The **Set-AzureRmDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="f759c-107">Il cmdlet restituisce l'oggetto ArtifactSource aggiornato.</span><span class="sxs-lookup"><span data-stu-id="f759c-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="f759c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f759c-108">EXAMPLES</span></span>

### <span data-ttu-id="f759c-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f759c-109">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="f759c-110">Questo comando aggiorna un'origine dell'elemento il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="f759c-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="f759c-111">L'origine dell'elemento verrà aggiornata alle proprietà impostate nel $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="f759c-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="f759c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f759c-112">PARAMETERS</span></span>

### <span data-ttu-id="f759c-113">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="f759c-113">-ArtifactSource</span></span>
<span data-ttu-id="f759c-114">Oggetto origine elemento.</span><span class="sxs-lookup"><span data-stu-id="f759c-114">The artifact source object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f759c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f759c-115">-DefaultProfile</span></span>
<span data-ttu-id="f759c-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f759c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f759c-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f759c-117">-Confirm</span></span>
<span data-ttu-id="f759c-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f759c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f759c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f759c-119">-WhatIf</span></span>
<span data-ttu-id="f759c-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f759c-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f759c-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f759c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f759c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f759c-122">CommonParameters</span></span>
<span data-ttu-id="f759c-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f759c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f759c-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f759c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f759c-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f759c-125">INPUTS</span></span>

### <span data-ttu-id="f759c-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="f759c-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="f759c-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f759c-127">OUTPUTS</span></span>

### <span data-ttu-id="f759c-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="f759c-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="f759c-129">Note</span><span class="sxs-lookup"><span data-stu-id="f759c-129">NOTES</span></span>

## <span data-ttu-id="f759c-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f759c-130">RELATED LINKS</span></span>

[<span data-ttu-id="f759c-131">New-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="f759c-131">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="f759c-132">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="f759c-132">Get-AzureRmDeploymentManagerArtifactSource</span></span>](./Get-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="f759c-133">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="f759c-133">Remove-AzureRmDeploymentManagerArtifactSource</span></span>](./Remove-AzureRmDeploymentManagerArtifactSource.md)