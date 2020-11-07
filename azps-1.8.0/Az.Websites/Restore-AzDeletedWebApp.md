---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: a90a56417ab8b1b08d72cb9d00ebe7411a6f075c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676262"
---
# <span data-ttu-id="1dba5-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1dba5-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="1dba5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1dba5-102">SYNOPSIS</span></span>
<span data-ttu-id="1dba5-103">Ripristina un'app Web eliminata in un'app Web nuova o esistente.</span><span class="sxs-lookup"><span data-stu-id="1dba5-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="1dba5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1dba5-104">SYNTAX</span></span>

### <span data-ttu-id="1dba5-105">FromDeletedResourceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1dba5-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dba5-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="1dba5-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1dba5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1dba5-107">DESCRIPTION</span></span>
<span data-ttu-id="1dba5-108">Il cmdlet **Restore-AzDeletedWebApp** ripristina un'app Web eliminata.</span><span class="sxs-lookup"><span data-stu-id="1dba5-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="1dba5-109">L'app Web specificata da TargetResourceGroupName, TargetName e TargetSlot verrà sovrascritta con il contenuto e le impostazioni dell'app Web eliminata.</span><span class="sxs-lookup"><span data-stu-id="1dba5-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="1dba5-110">Se i parametri di destinazione non vengono specificati, verranno automaticamente riempiti con il gruppo di risorse, il nome e lo slot dell'app Web eliminata.</span><span class="sxs-lookup"><span data-stu-id="1dba5-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="1dba5-111">Se l'app Web di destinazione non esiste, verrà creata automaticamente nel piano di servizio app specificato da TargetAppServicePlanName.</span><span class="sxs-lookup"><span data-stu-id="1dba5-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="1dba5-112">Il parametro RestoreContentOnly switch può essere usato per ripristinare solo i file dell'app eliminata senza le impostazioni dell'app.</span><span class="sxs-lookup"><span data-stu-id="1dba5-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="1dba5-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1dba5-113">EXAMPLES</span></span>

### <span data-ttu-id="1dba5-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1dba5-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="1dba5-115">Ripristina un'app eliminata denominata ContosoApp appartenente al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="1dba5-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="1dba5-116">Verrà creata una nuova app con lo stesso nome e il relativo gruppo di risorse nel piano di servizio app denominato ContosoPlan e verranno ripristinati i file e le impostazioni dell'app eliminata.</span><span class="sxs-lookup"><span data-stu-id="1dba5-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="1dba5-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1dba5-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="1dba5-118">Ripristina lo slot di staging di un'app eliminata denominata ContosoApp appartenente al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="1dba5-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="1dba5-119">L'app Web denominata ContosoRestore che appartiene al gruppo di risorse predefinito-Web-Eastus verrà sovrascritta.</span><span class="sxs-lookup"><span data-stu-id="1dba5-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="1dba5-120">Le impostazioni delle app Web eliminate non verranno ripristinate.</span><span class="sxs-lookup"><span data-stu-id="1dba5-120">The deleted web app settings will not be restored.</span></span>

## <span data-ttu-id="1dba5-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1dba5-121">PARAMETERS</span></span>

### <span data-ttu-id="1dba5-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1dba5-122">-AsJob</span></span>
<span data-ttu-id="1dba5-123">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1dba5-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1dba5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dba5-124">-DefaultProfile</span></span>
<span data-ttu-id="1dba5-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1dba5-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dba5-126">-Force</span><span class="sxs-lookup"><span data-stu-id="1dba5-126">-Force</span></span>
<span data-ttu-id="1dba5-127">Eseguire il ripristino senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="1dba5-127">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="1dba5-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dba5-128">-InputObject</span></span>
<span data-ttu-id="1dba5-129">L'app Web Azure eliminata.</span><span class="sxs-lookup"><span data-stu-id="1dba5-129">The deleted Azure Web App.</span></span>

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

### <span data-ttu-id="1dba5-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="1dba5-130">-Name</span></span>
<span data-ttu-id="1dba5-131">Nome dell'app Web Azure eliminata.</span><span class="sxs-lookup"><span data-stu-id="1dba5-131">The name of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="1dba5-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dba5-132">-ResourceGroupName</span></span>
<span data-ttu-id="1dba5-133">Gruppo risorse di Azure Web App eliminata.</span><span class="sxs-lookup"><span data-stu-id="1dba5-133">The resource group of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="1dba5-134">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="1dba5-134">-RestoreContentOnly</span></span>
<span data-ttu-id="1dba5-135">Ripristinare i file dell'app Web, ma non ripristinare le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="1dba5-135">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="1dba5-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="1dba5-136">-Slot</span></span>
<span data-ttu-id="1dba5-137">Slot di Azure Web App eliminato.</span><span class="sxs-lookup"><span data-stu-id="1dba5-137">The deleted Azure Web App slot.</span></span>

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

### <span data-ttu-id="1dba5-138">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="1dba5-138">-TargetAppServicePlanName</span></span>
<span data-ttu-id="1dba5-139">Piano del servizio app per la nuova app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="1dba5-139">The App Service Plan for the new Azure Web App.</span></span>

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

### <span data-ttu-id="1dba5-140">-TargetName</span><span class="sxs-lookup"><span data-stu-id="1dba5-140">-TargetName</span></span>
<span data-ttu-id="1dba5-141">Nome della nuova app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="1dba5-141">The name of the new Azure Web App.</span></span>

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

### <span data-ttu-id="1dba5-142">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dba5-142">-TargetResourceGroupName</span></span>
<span data-ttu-id="1dba5-143">Gruppo di risorse che contiene la nuova app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="1dba5-143">The resource group containing the new Azure Web App.</span></span>

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

### <span data-ttu-id="1dba5-144">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="1dba5-144">-TargetSlot</span></span>
<span data-ttu-id="1dba5-145">Nome del nuovo slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1dba5-145">The name of the new Azure Web App slot.</span></span>

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

### <span data-ttu-id="1dba5-146">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="1dba5-146">-UseDisasterRecovery</span></span>
<span data-ttu-id="1dba5-147">USA per recuperare un'app eliminata da un'unità di scala offline.</span><span class="sxs-lookup"><span data-stu-id="1dba5-147">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="1dba5-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1dba5-148">-Confirm</span></span>
<span data-ttu-id="1dba5-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dba5-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dba5-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dba5-150">-WhatIf</span></span>
<span data-ttu-id="1dba5-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dba5-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1dba5-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dba5-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dba5-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dba5-153">CommonParameters</span></span>
<span data-ttu-id="1dba5-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dba5-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dba5-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dba5-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dba5-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1dba5-156">INPUTS</span></span>

### <span data-ttu-id="1dba5-157">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1dba5-157">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="1dba5-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1dba5-158">OUTPUTS</span></span>

### <span data-ttu-id="1dba5-159">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="1dba5-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1dba5-160">Note</span><span class="sxs-lookup"><span data-stu-id="1dba5-160">NOTES</span></span>

## <span data-ttu-id="1dba5-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1dba5-161">RELATED LINKS</span></span>

[<span data-ttu-id="1dba5-162">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1dba5-162">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)