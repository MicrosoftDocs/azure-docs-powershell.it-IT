---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: 81807c92b336bd171d0890f5b3e948ec11313023
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002062"
---
# <span data-ttu-id="19c53-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="19c53-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="19c53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19c53-102">SYNOPSIS</span></span>
<span data-ttu-id="19c53-103">Ripristina un'app Web eliminata in un'app Web nuova o esistente.</span><span class="sxs-lookup"><span data-stu-id="19c53-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="19c53-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19c53-104">SYNTAX</span></span>

### <span data-ttu-id="19c53-105">FromDeletedResourceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="19c53-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-Location <String>]
 [-DeletedId <String>] [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19c53-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="19c53-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-DeletedId <String>] [-TargetName <String>] 
 [-TargetSlot <String>] [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] 
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> 
 [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19c53-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="19c53-107">DESCRIPTION</span></span>
<span data-ttu-id="19c53-108">Il cmdlet **Restore-AzDeletedWebApp** ripristina un'app Web eliminata.</span><span class="sxs-lookup"><span data-stu-id="19c53-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="19c53-109">L'app Web specificata da TargetResourceGroupName, TargetName e TargetSlot verrà sovrascritta con il contenuto e le impostazioni dell'app Web eliminata.</span><span class="sxs-lookup"><span data-stu-id="19c53-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="19c53-110">Se i parametri di destinazione non sono specificati, verranno inseriti automaticamente con il gruppo di risorse, il nome e lo slot dell'app Web eliminata.</span><span class="sxs-lookup"><span data-stu-id="19c53-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="19c53-111">Se l'app Web di destinazione non esiste, verrà creata automaticamente nel piano di servizio app specificato da TargetAppServicePlanName.</span><span class="sxs-lookup"><span data-stu-id="19c53-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="19c53-112">Il parametro RestoreContentOnly può essere usato per ripristinare solo i file dell'app eliminata senza le impostazioni dell'app.</span><span class="sxs-lookup"><span data-stu-id="19c53-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="19c53-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19c53-113">EXAMPLES</span></span>

### <span data-ttu-id="19c53-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="19c53-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="19c53-115">Ripristina un'app eliminata denominata ContosoApp appartenente al gruppo di risorse Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="19c53-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="19c53-116">Nel piano di servizio app denominato ContosoPlan verrà creata una nuova app con lo stesso nome e lo stesso gruppo di risorse e verranno ripristinati i file e le impostazioni dell'app eliminata.</span><span class="sxs-lookup"><span data-stu-id="19c53-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="19c53-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="19c53-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="19c53-118">Ripristina lo slot Di gestione temporanea di un'app eliminata denominata ContosoApp appartenente al gruppo di risorse Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="19c53-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="19c53-119">L'app Web denominata ContosoRestore appartenente al gruppo di risorse Default-Web-EastUS verrà sovrascritta.</span><span class="sxs-lookup"><span data-stu-id="19c53-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="19c53-120">Le impostazioni dell'app Web eliminate non verranno ripristinate.</span><span class="sxs-lookup"><span data-stu-id="19c53-120">The deleted web app settings will not be restored.</span></span>

###<span data-ttu-id="19c53-121">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="19c53-121">Example 3</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -DeletedId /subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Web/locations/location/deletedSites/1234 -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="19c53-122">Se vengono eliminate 2 app con lo stesso nome (ContosoApp), si ottengono i dettagli di entrambi i siti e si ripristina l'app denominata ContosoRestore con l'app desiderata chiamando Ripristina con l'ID.</span><span class="sxs-lookup"><span data-stu-id="19c53-122">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with Id.</span></span>

###<span data-ttu-id="19c53-123">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="19c53-123">Example 4</span></span>
```powershell
PS C:\> $deletedSite = Get-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp
PS C:\> Restore-AzDeletedWebApp -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -TargetAppServicePlanName ContosoPlan -InputObject $deletedSite[0]
```

<span data-ttu-id="19c53-124">Se sono presenti 2 app eliminate con lo stesso nome (ContosoApp), si ottengono i dettagli dei siti e si ripristina l'app denominata ContosoRestore con l'app desiderata chiamando ripristina con i dettagli di InputObject(Deletedsite)</span><span class="sxs-lookup"><span data-stu-id="19c53-124">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with InputObject(Deletedsite) details</span></span> 

## <span data-ttu-id="19c53-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19c53-125">PARAMETERS</span></span>

### <span data-ttu-id="19c53-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19c53-126">-AsJob</span></span>
<span data-ttu-id="19c53-127">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="19c53-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19c53-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19c53-128">-DefaultProfile</span></span>
<span data-ttu-id="19c53-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="19c53-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19c53-130">-DeletedId</span><span class="sxs-lookup"><span data-stu-id="19c53-130">-DeletedId</span></span>
<span data-ttu-id="19c53-131">ID dell'app Web di Azure eliminata.</span><span class="sxs-lookup"><span data-stu-id="19c53-131">The Id of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c53-132">-Force</span><span class="sxs-lookup"><span data-stu-id="19c53-132">-Force</span></span>
<span data-ttu-id="19c53-133">Eseguire il ripristino senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="19c53-133">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="19c53-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19c53-134">-InputObject</span></span>
<span data-ttu-id="19c53-135">App Web di Azure eliminata.</span><span class="sxs-lookup"><span data-stu-id="19c53-135">The deleted Azure Web App.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp
Parameter Sets: FromDeletedApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19c53-136">-Location</span><span class="sxs-lookup"><span data-stu-id="19c53-136">-Location</span></span>
<span data-ttu-id="19c53-137">Posizione dell'app Web di Azure eliminata.</span><span class="sxs-lookup"><span data-stu-id="19c53-137">The location of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c53-138">-Name</span><span class="sxs-lookup"><span data-stu-id="19c53-138">-Name</span></span>
<span data-ttu-id="19c53-139">Nome dell'app Web di Azure eliminata.</span><span class="sxs-lookup"><span data-stu-id="19c53-139">The name of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c53-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19c53-140">-ResourceGroupName</span></span>
<span data-ttu-id="19c53-141">Gruppo di risorse di Azure Web App eliminata.</span><span class="sxs-lookup"><span data-stu-id="19c53-141">The resource group of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c53-142">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="19c53-142">-RestoreContentOnly</span></span>
<span data-ttu-id="19c53-143">Ripristinare i file dell'app Web, ma non le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="19c53-143">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="19c53-144">-Slot</span><span class="sxs-lookup"><span data-stu-id="19c53-144">-Slot</span></span>
<span data-ttu-id="19c53-145">Slot di Azure Web App eliminato.</span><span class="sxs-lookup"><span data-stu-id="19c53-145">The deleted Azure Web App slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c53-146">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="19c53-146">-TargetAppServicePlanName</span></span>
<span data-ttu-id="19c53-147">Il piano di servizio app per la nuova app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="19c53-147">The App Service Plan for the new Azure Web App.</span></span>

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

### <span data-ttu-id="19c53-148">-TargetName</span><span class="sxs-lookup"><span data-stu-id="19c53-148">-TargetName</span></span>
<span data-ttu-id="19c53-149">Nome della nuova app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="19c53-149">The name of the new Azure Web App.</span></span>

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

### <span data-ttu-id="19c53-150">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19c53-150">-TargetResourceGroupName</span></span>
<span data-ttu-id="19c53-151">Gruppo di risorse che contiene la nuova app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="19c53-151">The resource group containing the new Azure Web App.</span></span>

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

### <span data-ttu-id="19c53-152">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="19c53-152">-TargetSlot</span></span>
<span data-ttu-id="19c53-153">Nome del nuovo slot per Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="19c53-153">The name of the new Azure Web App slot.</span></span>

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

### <span data-ttu-id="19c53-154">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="19c53-154">-UseDisasterRecovery</span></span>
<span data-ttu-id="19c53-155">Consente di recuperare un'app eliminata da un'unità di scala offline.</span><span class="sxs-lookup"><span data-stu-id="19c53-155">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="19c53-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19c53-156">-Confirm</span></span>
<span data-ttu-id="19c53-157">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19c53-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19c53-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19c53-158">-WhatIf</span></span>
<span data-ttu-id="19c53-159">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19c53-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19c53-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19c53-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19c53-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c53-161">CommonParameters</span></span>
<span data-ttu-id="19c53-162">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19c53-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c53-163">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19c53-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c53-164">INPUT</span><span class="sxs-lookup"><span data-stu-id="19c53-164">INPUTS</span></span>

### <span data-ttu-id="19c53-165">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="19c53-165">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="19c53-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19c53-166">OUTPUTS</span></span>

### <span data-ttu-id="19c53-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="19c53-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="19c53-168">NOTE</span><span class="sxs-lookup"><span data-stu-id="19c53-168">NOTES</span></span>

## <span data-ttu-id="19c53-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19c53-169">RELATED LINKS</span></span>

[<span data-ttu-id="19c53-170">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="19c53-170">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)