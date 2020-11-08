---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: 7cffc754e2662216aef10f163601e5d5a5339663
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190396"
---
# <span data-ttu-id="afe70-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="afe70-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="afe70-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="afe70-102">SYNOPSIS</span></span>
<span data-ttu-id="afe70-103">Ripristina un'app Web eliminata in un'app Web nuova o esistente.</span><span class="sxs-lookup"><span data-stu-id="afe70-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="afe70-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="afe70-104">SYNTAX</span></span>

### <span data-ttu-id="afe70-105">FromDeletedResourceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="afe70-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-Location <String>]
 [-DeletedId <String>] [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afe70-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="afe70-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-DeletedId <String>] [-TargetName <String>] 
 [-TargetSlot <String>] [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] 
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> 
 [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="afe70-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="afe70-107">DESCRIPTION</span></span>
<span data-ttu-id="afe70-108">Il cmdlet **Restore-AzDeletedWebApp** ripristina un'app Web eliminata.</span><span class="sxs-lookup"><span data-stu-id="afe70-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="afe70-109">L'app Web specificata da TargetResourceGroupName, TargetName e TargetSlot verrà sovrascritta con il contenuto e le impostazioni dell'app Web eliminata.</span><span class="sxs-lookup"><span data-stu-id="afe70-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="afe70-110">Se i parametri di destinazione non vengono specificati, verranno automaticamente riempiti con il gruppo di risorse, il nome e lo slot dell'app Web eliminata.</span><span class="sxs-lookup"><span data-stu-id="afe70-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="afe70-111">Se l'app Web di destinazione non esiste, verrà creata automaticamente nel piano di servizio app specificato da TargetAppServicePlanName.</span><span class="sxs-lookup"><span data-stu-id="afe70-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="afe70-112">Il parametro RestoreContentOnly switch può essere usato per ripristinare solo i file dell'app eliminata senza le impostazioni dell'app.</span><span class="sxs-lookup"><span data-stu-id="afe70-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="afe70-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="afe70-113">EXAMPLES</span></span>

### <span data-ttu-id="afe70-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="afe70-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="afe70-115">Ripristina un'app eliminata denominata ContosoApp appartenente al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="afe70-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="afe70-116">Verrà creata una nuova app con lo stesso nome e il relativo gruppo di risorse nel piano di servizio app denominato ContosoPlan e verranno ripristinati i file e le impostazioni dell'app eliminata.</span><span class="sxs-lookup"><span data-stu-id="afe70-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="afe70-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="afe70-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="afe70-118">Ripristina lo slot di staging di un'app eliminata denominata ContosoApp appartenente al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="afe70-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="afe70-119">L'app Web denominata ContosoRestore che appartiene al gruppo di risorse predefinito-Web-Eastus verrà sovrascritta.</span><span class="sxs-lookup"><span data-stu-id="afe70-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="afe70-120">Le impostazioni delle app Web eliminate non verranno ripristinate.</span><span class="sxs-lookup"><span data-stu-id="afe70-120">The deleted web app settings will not be restored.</span></span>

###<span data-ttu-id="afe70-121">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="afe70-121">Example 3</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -DeletedId /subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Web/locations/location/deletedSites/1234 -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="afe70-122">Nel caso in cui ci siano 2 App eliminate con lo stesso nome (ContosoApp), allora otteniamo i dettagli di entrambi i siti e ripristiniamo l'app denominata ContosoRestore con l'app di nostra scelta chiamando Restore con ID.</span><span class="sxs-lookup"><span data-stu-id="afe70-122">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with Id.</span></span>

###<span data-ttu-id="afe70-123">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="afe70-123">Example 4</span></span>
```powershell
PS C:\> $deletedSite = Get-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp
PS C:\> Restore-AzDeletedWebApp -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -TargetAppServicePlanName ContosoPlan -InputObject $deletedSite[0]
```

<span data-ttu-id="afe70-124">Nel caso in cui ci siano 2 App eliminate con lo stesso nome (ContosoApp), allora otteniamo i dettagli di entrambi i siti e ripristiniamo l'app denominata ContosoRestore con l'app di nostra scelta chiamando il ripristino con i dettagli di InputObject (Deletedsite)</span><span class="sxs-lookup"><span data-stu-id="afe70-124">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with InputObject(Deletedsite) details</span></span> 

## <span data-ttu-id="afe70-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="afe70-125">PARAMETERS</span></span>

### <span data-ttu-id="afe70-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="afe70-126">-AsJob</span></span>
<span data-ttu-id="afe70-127">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="afe70-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="afe70-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afe70-128">-DefaultProfile</span></span>
<span data-ttu-id="afe70-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="afe70-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afe70-130">-DeletedId</span><span class="sxs-lookup"><span data-stu-id="afe70-130">-DeletedId</span></span>
<span data-ttu-id="afe70-131">ID dell'app Web Azure eliminata.</span><span class="sxs-lookup"><span data-stu-id="afe70-131">The Id of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="afe70-132">-Force</span><span class="sxs-lookup"><span data-stu-id="afe70-132">-Force</span></span>
<span data-ttu-id="afe70-133">Eseguire il ripristino senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="afe70-133">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="afe70-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afe70-134">-InputObject</span></span>
<span data-ttu-id="afe70-135">L'app Web Azure eliminata.</span><span class="sxs-lookup"><span data-stu-id="afe70-135">The deleted Azure Web App.</span></span>

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

### <span data-ttu-id="afe70-136">-Posizione</span><span class="sxs-lookup"><span data-stu-id="afe70-136">-Location</span></span>
<span data-ttu-id="afe70-137">Posizione dell'app Web Azure eliminata.</span><span class="sxs-lookup"><span data-stu-id="afe70-137">The location of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="afe70-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="afe70-138">-Name</span></span>
<span data-ttu-id="afe70-139">Nome dell'app Web Azure eliminata.</span><span class="sxs-lookup"><span data-stu-id="afe70-139">The name of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="afe70-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afe70-140">-ResourceGroupName</span></span>
<span data-ttu-id="afe70-141">Gruppo risorse di Azure Web App eliminata.</span><span class="sxs-lookup"><span data-stu-id="afe70-141">The resource group of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="afe70-142">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="afe70-142">-RestoreContentOnly</span></span>
<span data-ttu-id="afe70-143">Ripristinare i file dell'app Web, ma non ripristinare le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="afe70-143">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="afe70-144">-Slot</span><span class="sxs-lookup"><span data-stu-id="afe70-144">-Slot</span></span>
<span data-ttu-id="afe70-145">Slot di Azure Web App eliminato.</span><span class="sxs-lookup"><span data-stu-id="afe70-145">The deleted Azure Web App slot.</span></span>

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

### <span data-ttu-id="afe70-146">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="afe70-146">-TargetAppServicePlanName</span></span>
<span data-ttu-id="afe70-147">Piano del servizio app per la nuova app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="afe70-147">The App Service Plan for the new Azure Web App.</span></span>

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

### <span data-ttu-id="afe70-148">-TargetName</span><span class="sxs-lookup"><span data-stu-id="afe70-148">-TargetName</span></span>
<span data-ttu-id="afe70-149">Nome della nuova app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="afe70-149">The name of the new Azure Web App.</span></span>

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

### <span data-ttu-id="afe70-150">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afe70-150">-TargetResourceGroupName</span></span>
<span data-ttu-id="afe70-151">Gruppo di risorse che contiene la nuova app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="afe70-151">The resource group containing the new Azure Web App.</span></span>

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

### <span data-ttu-id="afe70-152">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="afe70-152">-TargetSlot</span></span>
<span data-ttu-id="afe70-153">Nome del nuovo slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="afe70-153">The name of the new Azure Web App slot.</span></span>

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

### <span data-ttu-id="afe70-154">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="afe70-154">-UseDisasterRecovery</span></span>
<span data-ttu-id="afe70-155">USA per recuperare un'app eliminata da un'unità di scala offline.</span><span class="sxs-lookup"><span data-stu-id="afe70-155">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="afe70-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="afe70-156">-Confirm</span></span>
<span data-ttu-id="afe70-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afe70-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afe70-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afe70-158">-WhatIf</span></span>
<span data-ttu-id="afe70-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="afe70-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="afe70-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="afe70-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afe70-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afe70-161">CommonParameters</span></span>
<span data-ttu-id="afe70-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afe70-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afe70-163">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afe70-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afe70-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="afe70-164">INPUTS</span></span>

### <span data-ttu-id="afe70-165">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="afe70-165">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="afe70-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="afe70-166">OUTPUTS</span></span>

### <span data-ttu-id="afe70-167">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="afe70-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="afe70-168">Note</span><span class="sxs-lookup"><span data-stu-id="afe70-168">NOTES</span></span>

## <span data-ttu-id="afe70-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="afe70-169">RELATED LINKS</span></span>

[<span data-ttu-id="afe70-170">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="afe70-170">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)