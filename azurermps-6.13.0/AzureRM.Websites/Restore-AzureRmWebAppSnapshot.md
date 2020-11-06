---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppSnapshot.md
ms.openlocfilehash: 536d0fe0f32231bfd732698c584e02be95d5c20e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513288"
---
# <span data-ttu-id="389c0-101">Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="389c0-101">Restore-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="389c0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="389c0-102">SYNOPSIS</span></span>
<span data-ttu-id="389c0-103">Ripristina uno snapshot Web App.</span><span class="sxs-lookup"><span data-stu-id="389c0-103">Restores a web app snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="389c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="389c0-104">SYNTAX</span></span>

### <span data-ttu-id="389c0-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="389c0-105">FromResourceName</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="389c0-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="389c0-106">FromWebApp</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="389c0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="389c0-107">DESCRIPTION</span></span>
<span data-ttu-id="389c0-108">Consente di ripristinare uno snapshot di un'app Web nell'app Web.</span><span class="sxs-lookup"><span data-stu-id="389c0-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="389c0-109">Il ripristino di uno snapshot sovrascrive tutti i file in un'app Web con i file contenuti nello snapshot.</span><span class="sxs-lookup"><span data-stu-id="389c0-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="389c0-110">Per ripristinare anche le impostazioni, usa il parametro RecoverConfiguration switch.</span><span class="sxs-lookup"><span data-stu-id="389c0-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="389c0-111">Uno snapshot da un'app Web può essere ripristinato in qualsiasi altra app Web nello stesso abbonamento.</span><span class="sxs-lookup"><span data-stu-id="389c0-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="389c0-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="389c0-112">EXAMPLES</span></span>

### <span data-ttu-id="389c0-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="389c0-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="389c0-114">Ottiene lo snapshot più recente di un'app Web denominata "ContosoApp" con uno slot denominato "Staging" nel gruppo di risorse "default-Web-Westus".</span><span class="sxs-lookup"><span data-stu-id="389c0-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="389c0-115">Ripristina lo snapshot nello slot "ripristino" dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="389c0-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="389c0-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="389c0-116">PARAMETERS</span></span>

### <span data-ttu-id="389c0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="389c0-117">-AsJob</span></span>
<span data-ttu-id="389c0-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="389c0-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="389c0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="389c0-119">-DefaultProfile</span></span>
<span data-ttu-id="389c0-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="389c0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="389c0-121">-Force</span><span class="sxs-lookup"><span data-stu-id="389c0-121">-Force</span></span>
<span data-ttu-id="389c0-122">Consente di sovrascrivere l'app Web originale senza visualizzare un avviso.</span><span class="sxs-lookup"><span data-stu-id="389c0-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

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

### <span data-ttu-id="389c0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="389c0-123">-InputObject</span></span>
<span data-ttu-id="389c0-124">Lo snapshot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="389c0-124">The Azure Web App snapshot.</span></span>

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

### <span data-ttu-id="389c0-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="389c0-125">-Name</span></span>
<span data-ttu-id="389c0-126">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="389c0-126">The name of the web app.</span></span>

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

### <span data-ttu-id="389c0-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="389c0-127">-RecoverConfiguration</span></span>
<span data-ttu-id="389c0-128">Recupera la configurazione dell'app Web oltre ai file.</span><span class="sxs-lookup"><span data-stu-id="389c0-128">Recover the web app's configuration in addition to files.</span></span>

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

### <span data-ttu-id="389c0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="389c0-129">-ResourceGroupName</span></span>
<span data-ttu-id="389c0-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="389c0-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="389c0-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="389c0-131">-Slot</span></span>
<span data-ttu-id="389c0-132">Il nome dello slot Web App.</span><span class="sxs-lookup"><span data-stu-id="389c0-132">The name of the web app slot.</span></span>

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

### <span data-ttu-id="389c0-133">-Web App</span><span class="sxs-lookup"><span data-stu-id="389c0-133">-WebApp</span></span>
<span data-ttu-id="389c0-134">Oggetto app Web</span><span class="sxs-lookup"><span data-stu-id="389c0-134">The web app object</span></span>

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

### <span data-ttu-id="389c0-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="389c0-135">-Confirm</span></span>
<span data-ttu-id="389c0-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="389c0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="389c0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="389c0-137">-WhatIf</span></span>
<span data-ttu-id="389c0-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="389c0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="389c0-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="389c0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="389c0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="389c0-140">CommonParameters</span></span>
<span data-ttu-id="389c0-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="389c0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="389c0-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="389c0-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="389c0-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="389c0-143">INPUTS</span></span>

### <span data-ttu-id="389c0-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="389c0-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="389c0-145">System. String</span><span class="sxs-lookup"><span data-stu-id="389c0-145">System.String</span></span>

### <span data-ttu-id="389c0-146">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="389c0-146">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="389c0-147">Parametri: Web App (ByValue)</span><span class="sxs-lookup"><span data-stu-id="389c0-147">Parameters: WebApp (ByValue)</span></span>

### <span data-ttu-id="389c0-148">Microsoft. Azure. Commands. webapps. Cmdlets. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="389c0-148">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>
<span data-ttu-id="389c0-149">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="389c0-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="389c0-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="389c0-150">OUTPUTS</span></span>

### <span data-ttu-id="389c0-151">System. void</span><span class="sxs-lookup"><span data-stu-id="389c0-151">System.Void</span></span>

## <span data-ttu-id="389c0-152">Note</span><span class="sxs-lookup"><span data-stu-id="389c0-152">NOTES</span></span>

## <span data-ttu-id="389c0-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="389c0-153">RELATED LINKS</span></span>
