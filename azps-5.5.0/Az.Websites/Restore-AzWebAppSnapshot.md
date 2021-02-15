---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
ms.openlocfilehash: 1dd84305753edc8ad639c160c9003c4c393d041e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182423"
---
# <span data-ttu-id="8274a-101">Restore-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="8274a-101">Restore-AzWebAppSnapshot</span></span>

## <span data-ttu-id="8274a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8274a-102">SYNOPSIS</span></span>
<span data-ttu-id="8274a-103">Ripristina uno snapshot di un'app Web.</span><span class="sxs-lookup"><span data-stu-id="8274a-103">Restores a web app snapshot.</span></span>

## <span data-ttu-id="8274a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8274a-104">SYNTAX</span></span>

### <span data-ttu-id="8274a-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="8274a-105">FromResourceName</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8274a-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="8274a-106">FromWebApp</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8274a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8274a-107">DESCRIPTION</span></span>
<span data-ttu-id="8274a-108">Ripristina uno snapshot di un'app Web nell'app Web.</span><span class="sxs-lookup"><span data-stu-id="8274a-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="8274a-109">Il ripristino di uno snapshot sovrascrive tutti i file di un'app Web con i file contenuti nello snapshot.</span><span class="sxs-lookup"><span data-stu-id="8274a-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="8274a-110">Anche per ripristinare le impostazioni, usare il parametro RecoverConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8274a-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="8274a-111">È possibile ripristinare uno snapshot di un'app Web in qualsiasi altra app Web nello stesso abbonamento.</span><span class="sxs-lookup"><span data-stu-id="8274a-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="8274a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8274a-112">EXAMPLES</span></span>

### <span data-ttu-id="8274a-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8274a-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="8274a-114">Ottiene lo snapshot più recente di un'app Web denominata "ContosoApp" con uno slot denominato "Gestione temporanea" nel gruppo di risorse "Default-Web-WestUS".</span><span class="sxs-lookup"><span data-stu-id="8274a-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="8274a-115">Ripristina lo snapshot nello slot "Ripristina" dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="8274a-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="8274a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8274a-116">PARAMETERS</span></span>

### <span data-ttu-id="8274a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8274a-117">-AsJob</span></span>
<span data-ttu-id="8274a-118">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8274a-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8274a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8274a-119">-DefaultProfile</span></span>
<span data-ttu-id="8274a-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8274a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8274a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8274a-121">-Force</span></span>
<span data-ttu-id="8274a-122">Consente di sovrascrittura dell'app Web originale senza visualizzare un avviso.</span><span class="sxs-lookup"><span data-stu-id="8274a-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8274a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8274a-123">-InputObject</span></span>
<span data-ttu-id="8274a-124">Snapshot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="8274a-124">The Azure Web App snapshot.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8274a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8274a-125">-Name</span></span>
<span data-ttu-id="8274a-126">Il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="8274a-126">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8274a-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="8274a-127">-RecoverConfiguration</span></span>
<span data-ttu-id="8274a-128">Recuperare la configurazione dell'app Web oltre ai file.</span><span class="sxs-lookup"><span data-stu-id="8274a-128">Recover the web app's configuration in addition to files.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8274a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8274a-129">-ResourceGroupName</span></span>
<span data-ttu-id="8274a-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8274a-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8274a-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="8274a-131">-Slot</span></span>
<span data-ttu-id="8274a-132">Nome dello slot dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="8274a-132">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8274a-133">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="8274a-133">-UseDisasterRecovery</span></span>
<span data-ttu-id="8274a-134">Consente di recuperare uno snapshot da un'unità di scala offline.</span><span class="sxs-lookup"><span data-stu-id="8274a-134">Use to recover a snapshot from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="8274a-135">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8274a-135">-WebApp</span></span>
<span data-ttu-id="8274a-136">Oggetto app Web</span><span class="sxs-lookup"><span data-stu-id="8274a-136">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8274a-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8274a-137">-Confirm</span></span>
<span data-ttu-id="8274a-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8274a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8274a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8274a-139">-WhatIf</span></span>
<span data-ttu-id="8274a-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8274a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8274a-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8274a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8274a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8274a-142">CommonParameters</span></span>
<span data-ttu-id="8274a-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8274a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8274a-144">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8274a-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8274a-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="8274a-145">INPUTS</span></span>

### <span data-ttu-id="8274a-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8274a-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8274a-147">System.String</span><span class="sxs-lookup"><span data-stu-id="8274a-147">System.String</span></span>

### <span data-ttu-id="8274a-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="8274a-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="8274a-149">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="8274a-149">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="8274a-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8274a-150">OUTPUTS</span></span>

### <span data-ttu-id="8274a-151">System.Void</span><span class="sxs-lookup"><span data-stu-id="8274a-151">System.Void</span></span>

## <span data-ttu-id="8274a-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="8274a-152">NOTES</span></span>

## <span data-ttu-id="8274a-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8274a-153">RELATED LINKS</span></span>
