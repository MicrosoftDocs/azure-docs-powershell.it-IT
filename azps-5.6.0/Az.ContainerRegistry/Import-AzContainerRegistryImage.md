---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/import-azcontainerregistryimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
ms.openlocfilehash: 675bc66afd41e5db2ee356ad45ee2fdd9b3482f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963213"
---
# <span data-ttu-id="58106-101">Import-AzContainerRegistryImage</span><span class="sxs-lookup"><span data-stu-id="58106-101">Import-AzContainerRegistryImage</span></span>

## <span data-ttu-id="58106-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58106-102">SYNOPSIS</span></span>
<span data-ttu-id="58106-103">Importare un'immagine da un Registro di sistema pubblico/azure in un Registro di sistema del contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="58106-103">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="58106-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58106-104">SYNTAX</span></span>

### <span data-ttu-id="58106-105">ImportImageByResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58106-105">ImportImageByResourceId (Default)</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="58106-106">ImportImageByResourceIdWithCredential</span><span class="sxs-lookup"><span data-stu-id="58106-106">ImportImageByResourceIdWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-Username <String>] -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58106-107">ImportImageByRegistryUri</span><span class="sxs-lookup"><span data-stu-id="58106-107">ImportImageByRegistryUri</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58106-108">ImportImageByRegistryUriWithCredential</span><span class="sxs-lookup"><span data-stu-id="58106-108">ImportImageByRegistryUriWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-Username <String>] -Password <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="58106-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="58106-109">DESCRIPTION</span></span>
<span data-ttu-id="58106-110">Importare un'immagine da un Registro di sistema pubblico/azure in un Registro di sistema del contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="58106-110">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="58106-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58106-111">EXAMPLES</span></span>

### <span data-ttu-id="58106-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="58106-112">Example 1</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage library/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryUri docker.io -TargetTag busybox:latest
```

<span data-ttu-id="58106-113">Importare busybox in ACR.</span><span class="sxs-lookup"><span data-stu-id="58106-113">Import busybox to ACR.</span></span> <span data-ttu-id="58106-114">Nota:</span><span class="sxs-lookup"><span data-stu-id="58106-114">Note:</span></span> 
* <span data-ttu-id="58106-115">"raccolta/" deve essere aggiunto prima dell'immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="58106-115">"library/" need to be add before source image.</span></span> <span data-ttu-id="58106-116">"busybox:latest" => "library/busybox:latest"</span><span class="sxs-lookup"><span data-stu-id="58106-116">"busybox:latest" => "library/busybox:latest"</span></span>
* <span data-ttu-id="58106-117">Credenziali necessarie se il Registro di sistema di origine non è disponibile pubblicamente</span><span class="sxs-lookup"><span data-stu-id="58106-117">Credential needed if source registry is not publicly available</span></span>

### <span data-ttu-id="58106-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="58106-118">Example 2</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage $SourceRegistry.azurecr.io/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryResourceId $SourceACRID -TargetTag busybox:latest
```

<span data-ttu-id="58106-119">Importare Busybox dall'ACR di origine all'ACR di destinazione.</span><span class="sxs-lookup"><span data-stu-id="58106-119">Import busybox from source ACR to target ACR.</span></span> <span data-ttu-id="58106-120">Nota:</span><span class="sxs-lookup"><span data-stu-id="58106-120">Note:</span></span> 
* <span data-ttu-id="58106-121">Credenziali necessarie se l'utente amministratore per il Registro di sistema di origine è stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="58106-121">Credential needed if admin user for source registry was disabled.</span></span>

## <span data-ttu-id="58106-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58106-122">PARAMETERS</span></span>

### <span data-ttu-id="58106-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58106-123">-DefaultProfile</span></span>
<span data-ttu-id="58106-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58106-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58106-125">-Mode</span><span class="sxs-lookup"><span data-stu-id="58106-125">-Mode</span></span>
<span data-ttu-id="58106-126">Quando forza, i tag di destinazione esistenti vengono sovrascritti.</span><span class="sxs-lookup"><span data-stu-id="58106-126">When Force, any existing target tags will be overwritten.</span></span>
<span data-ttu-id="58106-127">Quando NoForce, tutti i tag di destinazione esistenti non riusciranno a eseguire l'operazione prima dell'inizio della copia.</span><span class="sxs-lookup"><span data-stu-id="58106-127">When NoForce, any existing target tags will fail the operation before any copying begins.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Force, NoForce

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58106-128">-Password</span><span class="sxs-lookup"><span data-stu-id="58106-128">-Password</span></span>
<span data-ttu-id="58106-129">Password usata per eseguire l'autenticazione con il Registro di sistema di origine.</span><span class="sxs-lookup"><span data-stu-id="58106-129">The password used to authenticate with the source registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceIdWithCredential, ImportImageByRegistryUriWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58106-130">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="58106-130">-RegistryName</span></span>
<span data-ttu-id="58106-131">Nome del Registro di sistema di destinazione.</span><span class="sxs-lookup"><span data-stu-id="58106-131">Target registry name.</span></span>

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

### <span data-ttu-id="58106-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58106-132">-ResourceGroupName</span></span>
<span data-ttu-id="58106-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="58106-133">Resource group name.</span></span>

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

### <span data-ttu-id="58106-134">-SourceImage</span><span class="sxs-lookup"><span data-stu-id="58106-134">-SourceImage</span></span>
<span data-ttu-id="58106-135">Nome archivio dell'immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="58106-135">Repository name of the source image.</span></span>

<span data-ttu-id="58106-136">Specificare un'immagine in base al repository ('hello-world').</span><span class="sxs-lookup"><span data-stu-id="58106-136">Specify an image by repository ('hello-world').</span></span>
<span data-ttu-id="58106-137">Verrà utilizzato il tag "più recente".</span><span class="sxs-lookup"><span data-stu-id="58106-137">This will use the 'latest' tag.</span></span>

<span data-ttu-id="58106-138">Specificare un'immagine in base al tag ('hello-world:latest').</span><span class="sxs-lookup"><span data-stu-id="58106-138">Specify an image by tag ('hello-world:latest').</span></span>

<span data-ttu-id="58106-139">Specificare un'immagine in base al digest del manifesto basato su sha256 (' hello-world@sha256:abc123 ').</span><span class="sxs-lookup"><span data-stu-id="58106-139">Specify an image by sha256-based manifest digest ('hello-world@sha256:abc123').</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58106-140">-SourceRegistryResourceId</span><span class="sxs-lookup"><span data-stu-id="58106-140">-SourceRegistryResourceId</span></span>
<span data-ttu-id="58106-141">Identificatore di risorsa del Registro di sistema del contenitore di Azure di origine.</span><span class="sxs-lookup"><span data-stu-id="58106-141">The resource identifier of the source Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceId, ImportImageByResourceIdWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58106-142">-SourceRegistryUri</span><span class="sxs-lookup"><span data-stu-id="58106-142">-SourceRegistryUri</span></span>
<span data-ttu-id="58106-143">Indirizzo del Registro di sistema di origine (ad esempio "mcr.microsoft.com").</span><span class="sxs-lookup"><span data-stu-id="58106-143">The address of the source registry (e.g. 'mcr.microsoft.com').</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByRegistryUri, ImportImageByRegistryUriWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58106-144">-TargetTag</span><span class="sxs-lookup"><span data-stu-id="58106-144">-TargetTag</span></span>
<span data-ttu-id="58106-145">Elenco di stringhe del formato repo \[ \] :tag.</span><span class="sxs-lookup"><span data-stu-id="58106-145">List of strings of the form repo\[:tag\].</span></span>
<span data-ttu-id="58106-146">Quando il tag viene omesso, verrà usato il tag di origine (o "più recente" se viene omesso anche il tag di origine).</span><span class="sxs-lookup"><span data-stu-id="58106-146">When tag is omitted the source will be used (or 'latest' if source tag is also omitted).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58106-147">-UntaggedTargetRepository</span><span class="sxs-lookup"><span data-stu-id="58106-147">-UntaggedTargetRepository</span></span>
<span data-ttu-id="58106-148">Elenco di stringhe di nomi di repository per eseguire solo una copia manifesto.</span><span class="sxs-lookup"><span data-stu-id="58106-148">List of strings of repository names to do a manifest only copy.</span></span>
<span data-ttu-id="58106-149">Non verrà creato alcun contrassegno.</span><span class="sxs-lookup"><span data-stu-id="58106-149">No tag will be created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58106-150">-Username</span><span class="sxs-lookup"><span data-stu-id="58106-150">-Username</span></span>
<span data-ttu-id="58106-151">Nome utente per l'autenticazione con il Registro di sistema di origine.</span><span class="sxs-lookup"><span data-stu-id="58106-151">The username to authenticate with the source registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceIdWithCredential, ImportImageByRegistryUriWithCredential
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58106-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58106-152">-Confirm</span></span>
<span data-ttu-id="58106-153">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58106-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58106-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58106-154">-WhatIf</span></span>
<span data-ttu-id="58106-155">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58106-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58106-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58106-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58106-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58106-157">CommonParameters</span></span>
<span data-ttu-id="58106-158">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58106-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58106-159">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="58106-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58106-160">INPUT</span><span class="sxs-lookup"><span data-stu-id="58106-160">INPUTS</span></span>

### <span data-ttu-id="58106-161">System.String</span><span class="sxs-lookup"><span data-stu-id="58106-161">System.String</span></span>

## <span data-ttu-id="58106-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58106-162">OUTPUTS</span></span>

### <span data-ttu-id="58106-163">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="58106-163">System.Boolean</span></span>

## <span data-ttu-id="58106-164">NOTE</span><span class="sxs-lookup"><span data-stu-id="58106-164">NOTES</span></span>

## <span data-ttu-id="58106-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58106-165">RELATED LINKS</span></span>
