---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/import-azcontainerregistryimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
ms.openlocfilehash: 5fee8fec8d7b87629bfa46932662f430534fc695
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477571"
---
# <span data-ttu-id="7546c-101">Import-AzContainerRegistryImage</span><span class="sxs-lookup"><span data-stu-id="7546c-101">Import-AzContainerRegistryImage</span></span>

## <span data-ttu-id="7546c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7546c-102">SYNOPSIS</span></span>
<span data-ttu-id="7546c-103">Importare immagini da un registro di sistema pubblico/Azure in un registro di sistema di Azure.</span><span class="sxs-lookup"><span data-stu-id="7546c-103">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="7546c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7546c-104">SYNTAX</span></span>

### <span data-ttu-id="7546c-105">ImportImageByResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7546c-105">ImportImageByResourceId (Default)</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7546c-106">ImportImageByResourceIdWithCredential</span><span class="sxs-lookup"><span data-stu-id="7546c-106">ImportImageByResourceIdWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-Username <String>] -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7546c-107">ImportImageByRegistryUri</span><span class="sxs-lookup"><span data-stu-id="7546c-107">ImportImageByRegistryUri</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7546c-108">ImportImageByRegistryUriWithCredential</span><span class="sxs-lookup"><span data-stu-id="7546c-108">ImportImageByRegistryUriWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-Username <String>] -Password <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7546c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7546c-109">DESCRIPTION</span></span>
<span data-ttu-id="7546c-110">Importare immagini da un registro di sistema pubblico/Azure in un registro di sistema di Azure.</span><span class="sxs-lookup"><span data-stu-id="7546c-110">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="7546c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7546c-111">EXAMPLES</span></span>

### <span data-ttu-id="7546c-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7546c-112">Example 1</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage library/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryUri docker.io -TargetTag busybox:latest
```

<span data-ttu-id="7546c-113">Importare busybox in ACR.</span><span class="sxs-lookup"><span data-stu-id="7546c-113">Import busybox to ACR.</span></span> <span data-ttu-id="7546c-114">Nota</span><span class="sxs-lookup"><span data-stu-id="7546c-114">Note:</span></span> 
* <span data-ttu-id="7546c-115">"raccolta/" deve essere aggiunta prima dell'immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="7546c-115">"library/" need to be add before source image.</span></span> <span data-ttu-id="7546c-116">"BUSYBOX: Ultima" => "raccolta/BUSYBOX: Ultima"</span><span class="sxs-lookup"><span data-stu-id="7546c-116">"busybox:latest" => "library/busybox:latest"</span></span>
* <span data-ttu-id="7546c-117">Credenziali necessarie se il registro di sistema di origine non è disponibile pubblicamente</span><span class="sxs-lookup"><span data-stu-id="7546c-117">Credential needed if source registry is not publicly available</span></span>

### <span data-ttu-id="7546c-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7546c-118">Example 2</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage $SourceRegistry.azurecr.io/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryResourceId $SourceACRID -TargetTag busybox:latest
```

<span data-ttu-id="7546c-119">Importare busybox da ACR di origine a target ACR.</span><span class="sxs-lookup"><span data-stu-id="7546c-119">Import busybox from source ACR to target ACR.</span></span> <span data-ttu-id="7546c-120">Nota</span><span class="sxs-lookup"><span data-stu-id="7546c-120">Note:</span></span> 
* <span data-ttu-id="7546c-121">Credenziali necessarie se l'utente amministratore per il registro di sistema di origine è stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="7546c-121">Credential needed if admin user for source registry was disabled.</span></span>

## <span data-ttu-id="7546c-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7546c-122">PARAMETERS</span></span>

### <span data-ttu-id="7546c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7546c-123">-DefaultProfile</span></span>
<span data-ttu-id="7546c-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7546c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7546c-125">-Modalità</span><span class="sxs-lookup"><span data-stu-id="7546c-125">-Mode</span></span>
<span data-ttu-id="7546c-126">Quando forza, eventuali contrassegni di destinazione esistenti verranno sovrascritti.</span><span class="sxs-lookup"><span data-stu-id="7546c-126">When Force, any existing target tags will be overwritten.</span></span>
<span data-ttu-id="7546c-127">Quando noforce, gli eventuali contrassegni di destinazione esistenti non riescono all'operazione prima che venga avviata la copia.</span><span class="sxs-lookup"><span data-stu-id="7546c-127">When NoForce, any existing target tags will fail the operation before any copying begins.</span></span>

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

### <span data-ttu-id="7546c-128">-Password</span><span class="sxs-lookup"><span data-stu-id="7546c-128">-Password</span></span>
<span data-ttu-id="7546c-129">Password usata per l'autenticazione con il registro di sistema di origine.</span><span class="sxs-lookup"><span data-stu-id="7546c-129">The password used to authenticate with the source registry.</span></span>

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

### <span data-ttu-id="7546c-130">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="7546c-130">-RegistryName</span></span>
<span data-ttu-id="7546c-131">Nome del registro di sistema di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7546c-131">Target registry name.</span></span>

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

### <span data-ttu-id="7546c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7546c-132">-ResourceGroupName</span></span>
<span data-ttu-id="7546c-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7546c-133">Resource group name.</span></span>

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

### <span data-ttu-id="7546c-134">-SourceImage</span><span class="sxs-lookup"><span data-stu-id="7546c-134">-SourceImage</span></span>
<span data-ttu-id="7546c-135">Nome del repository dell'immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="7546c-135">Repository name of the source image.</span></span>

<span data-ttu-id="7546c-136">Specificare un'immagine per repository (' Hello-World ').</span><span class="sxs-lookup"><span data-stu-id="7546c-136">Specify an image by repository ('hello-world').</span></span>
<span data-ttu-id="7546c-137">Verrà usato il tag "ultima".</span><span class="sxs-lookup"><span data-stu-id="7546c-137">This will use the 'latest' tag.</span></span>

<span data-ttu-id="7546c-138">Specificare un'immagine per tag (' Hello-World: Ultima ').</span><span class="sxs-lookup"><span data-stu-id="7546c-138">Specify an image by tag ('hello-world:latest').</span></span>

<span data-ttu-id="7546c-139">Specifica un'immagine in base al digest del manifesto basato su SHA256 (' hello-world@sha256:abc123 ').</span><span class="sxs-lookup"><span data-stu-id="7546c-139">Specify an image by sha256-based manifest digest ('hello-world@sha256:abc123').</span></span>

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

### <span data-ttu-id="7546c-140">-SourceRegistryResourceId</span><span class="sxs-lookup"><span data-stu-id="7546c-140">-SourceRegistryResourceId</span></span>
<span data-ttu-id="7546c-141">Identificatore delle risorse del registro di sistema del contenitore di Azure di origine.</span><span class="sxs-lookup"><span data-stu-id="7546c-141">The resource identifier of the source Azure Container Registry.</span></span>

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

### <span data-ttu-id="7546c-142">-SourceRegistryUri</span><span class="sxs-lookup"><span data-stu-id="7546c-142">-SourceRegistryUri</span></span>
<span data-ttu-id="7546c-143">Indirizzo del registro di sistema di origine (ad esempio, "mcr.microsoft.com").</span><span class="sxs-lookup"><span data-stu-id="7546c-143">The address of the source registry (e.g. 'mcr.microsoft.com').</span></span>

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

### <span data-ttu-id="7546c-144">-TargetTag</span><span class="sxs-lookup"><span data-stu-id="7546c-144">-TargetTag</span></span>
<span data-ttu-id="7546c-145">Elenco di stringhe del modulo repo \[ : tag \] .</span><span class="sxs-lookup"><span data-stu-id="7546c-145">List of strings of the form repo\[:tag\].</span></span>
<span data-ttu-id="7546c-146">Quando tag viene omesso, verrà usata l'origine (o "ultima" Se viene omesso anche il tag di origine).</span><span class="sxs-lookup"><span data-stu-id="7546c-146">When tag is omitted the source will be used (or 'latest' if source tag is also omitted).</span></span>

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

### <span data-ttu-id="7546c-147">-UntaggedTargetRepository</span><span class="sxs-lookup"><span data-stu-id="7546c-147">-UntaggedTargetRepository</span></span>
<span data-ttu-id="7546c-148">Elenco di stringhe di nomi di repository per eseguire una copia solo manifesto.</span><span class="sxs-lookup"><span data-stu-id="7546c-148">List of strings of repository names to do a manifest only copy.</span></span>
<span data-ttu-id="7546c-149">Nessun tag verrà creato.</span><span class="sxs-lookup"><span data-stu-id="7546c-149">No tag will be created.</span></span>

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

### <span data-ttu-id="7546c-150">-Username</span><span class="sxs-lookup"><span data-stu-id="7546c-150">-Username</span></span>
<span data-ttu-id="7546c-151">Il nome utente per l'autenticazione con il registro di sistema di origine.</span><span class="sxs-lookup"><span data-stu-id="7546c-151">The username to authenticate with the source registry.</span></span>

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

### <span data-ttu-id="7546c-152">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7546c-152">-Confirm</span></span>
<span data-ttu-id="7546c-153">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7546c-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7546c-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7546c-154">-WhatIf</span></span>
<span data-ttu-id="7546c-155">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7546c-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7546c-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7546c-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7546c-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7546c-157">CommonParameters</span></span>
<span data-ttu-id="7546c-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7546c-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7546c-159">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7546c-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7546c-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7546c-160">INPUTS</span></span>

### <span data-ttu-id="7546c-161">System. String</span><span class="sxs-lookup"><span data-stu-id="7546c-161">System.String</span></span>

## <span data-ttu-id="7546c-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7546c-162">OUTPUTS</span></span>

### <span data-ttu-id="7546c-163">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7546c-163">System.Boolean</span></span>

## <span data-ttu-id="7546c-164">Note</span><span class="sxs-lookup"><span data-stu-id="7546c-164">NOTES</span></span>

## <span data-ttu-id="7546c-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7546c-165">RELATED LINKS</span></span>
