---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmDeletedWebApp.md
ms.openlocfilehash: caebbe3c9b84b469e5fc357686b256aca59c2b61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516299"
---
# <span data-ttu-id="c8175-101">Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="c8175-101">Restore-AzureRmDeletedWebApp</span></span>

## <span data-ttu-id="c8175-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c8175-102">SYNOPSIS</span></span>
<span data-ttu-id="c8175-103">Ripristina un'app Web eliminata in un'app Web nuova o esistente.</span><span class="sxs-lookup"><span data-stu-id="c8175-103">Restores a deleted web app to a new or existing web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8175-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8175-104">SYNTAX</span></span>

### <span data-ttu-id="c8175-105">FromDeletedResourceName</span><span class="sxs-lookup"><span data-stu-id="c8175-105">FromDeletedResourceName</span></span>
```
Restore-AzureRmDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8175-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="c8175-106">FromDeletedApp</span></span>
```
Restore-AzureRmDeletedWebApp [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> [<CommonParameters>]
```

## <span data-ttu-id="c8175-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8175-107">DESCRIPTION</span></span>
<span data-ttu-id="c8175-108">Il cmdlet **Restore-AzureRmDeletedWebApp** ripristina un'app Web eliminata.</span><span class="sxs-lookup"><span data-stu-id="c8175-108">The **Restore-AzureRmDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="c8175-109">L'app Web specificata da TargetResourceGroupName, TargetName e TargetSlot verrà sovrascritta con il contenuto e le impostazioni dell'app Web eliminata.</span><span class="sxs-lookup"><span data-stu-id="c8175-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="c8175-110">Se i parametri di destinazione non vengono specificati, verranno automaticamente riempiti con il gruppo di risorse, il nome e lo slot dell'app Web eliminata.</span><span class="sxs-lookup"><span data-stu-id="c8175-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="c8175-111">Se l'app Web di destinazione non esiste, verrà creata automaticamente nel piano di servizio app specificato da TargetAppServicePlanName.</span><span class="sxs-lookup"><span data-stu-id="c8175-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="c8175-112">Il parametro RestoreContentOnly switch può essere usato per ripristinare solo i file dell'app eliminata senza le impostazioni dell'app.</span><span class="sxs-lookup"><span data-stu-id="c8175-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="c8175-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8175-113">EXAMPLES</span></span>

### <span data-ttu-id="c8175-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c8175-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzureRmDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="c8175-115">Ripristina un'app eliminata denominata ContosoApp appartenente al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="c8175-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="c8175-116">Verrà creata una nuova app con lo stesso nome e il relativo gruppo di risorse nel piano di servizio app denominato ContosoPlan e verranno ripristinati i file e le impostazioni dell'app eliminata.</span><span class="sxs-lookup"><span data-stu-id="c8175-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="c8175-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c8175-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzureRmDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="c8175-118">Ripristina lo slot di staging di un'app eliminata denominata ContosoApp appartenente al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="c8175-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="c8175-119">L'app Web denominata ContosoRestore che appartiene al gruppo di risorse predefinito-Web-Eastus verrà sovrascritta.</span><span class="sxs-lookup"><span data-stu-id="c8175-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="c8175-120">Le impostazioni delle app Web eliminate non verranno ripristinate.</span><span class="sxs-lookup"><span data-stu-id="c8175-120">The deleted web app settings will not be restored.</span></span>

## <span data-ttu-id="c8175-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8175-121">PARAMETERS</span></span>

### <span data-ttu-id="c8175-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8175-122">-AsJob</span></span>
<span data-ttu-id="c8175-123">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c8175-123">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8175-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8175-124">-DefaultProfile</span></span>
<span data-ttu-id="c8175-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c8175-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8175-126">-Force</span><span class="sxs-lookup"><span data-stu-id="c8175-126">-Force</span></span>
<span data-ttu-id="c8175-127">Eseguire il ripristino senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="c8175-127">Do the restore without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8175-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8175-128">-InputObject</span></span>
<span data-ttu-id="c8175-129">L'app Web Azure eliminata.</span><span class="sxs-lookup"><span data-stu-id="c8175-129">The deleted Azure Web App.</span></span>

```yaml
Type: PSAzureDeletedWebApp
Parameter Sets: FromDeletedApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8175-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8175-130">-Name</span></span>
<span data-ttu-id="c8175-131">Nome dell'app Web Azure eliminata.</span><span class="sxs-lookup"><span data-stu-id="c8175-131">The name of the deleted Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8175-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8175-132">-ResourceGroupName</span></span>
<span data-ttu-id="c8175-133">Gruppo risorse di Azure Web App eliminata.</span><span class="sxs-lookup"><span data-stu-id="c8175-133">The resource group of the deleted Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8175-134">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="c8175-134">-RestoreContentOnly</span></span>
<span data-ttu-id="c8175-135">Ripristinare i file dell'app Web, ma non ripristinare le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="c8175-135">Restore the web app's files, but do not restore the settings.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8175-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="c8175-136">-Slot</span></span>
<span data-ttu-id="c8175-137">Slot di Azure Web App eliminato.</span><span class="sxs-lookup"><span data-stu-id="c8175-137">The deleted Azure Web App slot.</span></span>

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8175-138">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="c8175-138">-TargetAppServicePlanName</span></span>
<span data-ttu-id="c8175-139">Piano del servizio app per la nuova app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="c8175-139">The App Service Plan for the new Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8175-140">-TargetName</span><span class="sxs-lookup"><span data-stu-id="c8175-140">-TargetName</span></span>
<span data-ttu-id="c8175-141">Nome della nuova app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="c8175-141">The name of the new Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8175-142">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8175-142">-TargetResourceGroupName</span></span>
<span data-ttu-id="c8175-143">Gruppo di risorse che contiene la nuova app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="c8175-143">The resource group containing the new Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8175-144">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="c8175-144">-TargetSlot</span></span>
<span data-ttu-id="c8175-145">Nome del nuovo slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c8175-145">The name of the new Azure Web App slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8175-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8175-146">CommonParameters</span></span>
<span data-ttu-id="c8175-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8175-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c8175-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8175-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8175-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c8175-149">INPUTS</span></span>

### <span data-ttu-id="c8175-150">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="c8175-150">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="c8175-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8175-151">OUTPUTS</span></span>

### <span data-ttu-id="c8175-152">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="c8175-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c8175-153">Note</span><span class="sxs-lookup"><span data-stu-id="c8175-153">NOTES</span></span>

## <span data-ttu-id="c8175-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8175-154">RELATED LINKS</span></span>

[<span data-ttu-id="c8175-155">Get-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="c8175-155">Get-AzureRmDeletedWebApp</span></span>](./Get-AzureRmDeletedWebApp.md)
