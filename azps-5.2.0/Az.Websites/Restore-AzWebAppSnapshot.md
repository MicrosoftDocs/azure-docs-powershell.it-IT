---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
ms.openlocfilehash: 1dd84305753edc8ad639c160c9003c4c393d041e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325956"
---
# <span data-ttu-id="744d5-101">Restore-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="744d5-101">Restore-AzWebAppSnapshot</span></span>

## <span data-ttu-id="744d5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="744d5-102">SYNOPSIS</span></span>
<span data-ttu-id="744d5-103">Ripristina uno snapshot Web App.</span><span class="sxs-lookup"><span data-stu-id="744d5-103">Restores a web app snapshot.</span></span>

## <span data-ttu-id="744d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="744d5-104">SYNTAX</span></span>

### <span data-ttu-id="744d5-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="744d5-105">FromResourceName</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="744d5-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="744d5-106">FromWebApp</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="744d5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="744d5-107">DESCRIPTION</span></span>
<span data-ttu-id="744d5-108">Consente di ripristinare uno snapshot di un'app Web nell'app Web.</span><span class="sxs-lookup"><span data-stu-id="744d5-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="744d5-109">Il ripristino di uno snapshot sovrascrive tutti i file in un'app Web con i file contenuti nello snapshot.</span><span class="sxs-lookup"><span data-stu-id="744d5-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="744d5-110">Per ripristinare anche le impostazioni, usa il parametro RecoverConfiguration switch.</span><span class="sxs-lookup"><span data-stu-id="744d5-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="744d5-111">Uno snapshot da un'app Web può essere ripristinato in qualsiasi altra app Web nello stesso abbonamento.</span><span class="sxs-lookup"><span data-stu-id="744d5-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="744d5-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="744d5-112">EXAMPLES</span></span>

### <span data-ttu-id="744d5-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="744d5-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="744d5-114">Ottiene lo snapshot più recente di un'app Web denominata "ContosoApp" con uno slot denominato "Staging" nel gruppo di risorse "default-Web-Westus".</span><span class="sxs-lookup"><span data-stu-id="744d5-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="744d5-115">Ripristina lo snapshot nello slot "ripristino" dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="744d5-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="744d5-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="744d5-116">PARAMETERS</span></span>

### <span data-ttu-id="744d5-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="744d5-117">-AsJob</span></span>
<span data-ttu-id="744d5-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="744d5-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="744d5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="744d5-119">-DefaultProfile</span></span>
<span data-ttu-id="744d5-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="744d5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="744d5-121">-Force</span><span class="sxs-lookup"><span data-stu-id="744d5-121">-Force</span></span>
<span data-ttu-id="744d5-122">Consente di sovrascrivere l'app Web originale senza visualizzare un avviso.</span><span class="sxs-lookup"><span data-stu-id="744d5-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

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

### <span data-ttu-id="744d5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="744d5-123">-InputObject</span></span>
<span data-ttu-id="744d5-124">Lo snapshot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="744d5-124">The Azure Web App snapshot.</span></span>

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

### <span data-ttu-id="744d5-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="744d5-125">-Name</span></span>
<span data-ttu-id="744d5-126">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="744d5-126">The name of the web app.</span></span>

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

### <span data-ttu-id="744d5-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="744d5-127">-RecoverConfiguration</span></span>
<span data-ttu-id="744d5-128">Recupera la configurazione dell'app Web oltre ai file.</span><span class="sxs-lookup"><span data-stu-id="744d5-128">Recover the web app's configuration in addition to files.</span></span>

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

### <span data-ttu-id="744d5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="744d5-129">-ResourceGroupName</span></span>
<span data-ttu-id="744d5-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="744d5-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="744d5-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="744d5-131">-Slot</span></span>
<span data-ttu-id="744d5-132">Il nome dello slot Web App.</span><span class="sxs-lookup"><span data-stu-id="744d5-132">The name of the web app slot.</span></span>

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

### <span data-ttu-id="744d5-133">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="744d5-133">-UseDisasterRecovery</span></span>
<span data-ttu-id="744d5-134">Consente di recuperare uno snapshot da un'unità di scala offline.</span><span class="sxs-lookup"><span data-stu-id="744d5-134">Use to recover a snapshot from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="744d5-135">-Web App</span><span class="sxs-lookup"><span data-stu-id="744d5-135">-WebApp</span></span>
<span data-ttu-id="744d5-136">Oggetto app Web</span><span class="sxs-lookup"><span data-stu-id="744d5-136">The web app object</span></span>

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

### <span data-ttu-id="744d5-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="744d5-137">-Confirm</span></span>
<span data-ttu-id="744d5-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="744d5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="744d5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="744d5-139">-WhatIf</span></span>
<span data-ttu-id="744d5-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="744d5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="744d5-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="744d5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="744d5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="744d5-142">CommonParameters</span></span>
<span data-ttu-id="744d5-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="744d5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="744d5-144">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="744d5-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="744d5-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="744d5-145">INPUTS</span></span>

### <span data-ttu-id="744d5-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="744d5-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="744d5-147">System. String</span><span class="sxs-lookup"><span data-stu-id="744d5-147">System.String</span></span>

### <span data-ttu-id="744d5-148">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="744d5-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="744d5-149">Microsoft. Azure. Commands. webapps. Cmdlets. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="744d5-149">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="744d5-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="744d5-150">OUTPUTS</span></span>

### <span data-ttu-id="744d5-151">System. void</span><span class="sxs-lookup"><span data-stu-id="744d5-151">System.Void</span></span>

## <span data-ttu-id="744d5-152">Note</span><span class="sxs-lookup"><span data-stu-id="744d5-152">NOTES</span></span>

## <span data-ttu-id="744d5-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="744d5-153">RELATED LINKS</span></span>
