---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappsnapshot
schema: 2.0.0
ms.openlocfilehash: 0719210cae275dc7e250e7fd14e622c51014d7c2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866785"
---
# <span data-ttu-id="fd44d-101">Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="fd44d-101">Restore-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="fd44d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fd44d-102">SYNOPSIS</span></span>
<span data-ttu-id="fd44d-103">Ripristina uno snapshot Web App.</span><span class="sxs-lookup"><span data-stu-id="fd44d-103">Restores a web app snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd44d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd44d-104">SYNTAX</span></span>

### <span data-ttu-id="fd44d-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="fd44d-105">FromResourceName</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd44d-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="fd44d-106">FromWebApp</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd44d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd44d-107">DESCRIPTION</span></span>
<span data-ttu-id="fd44d-108">Consente di ripristinare uno snapshot di un'app Web nell'app Web.</span><span class="sxs-lookup"><span data-stu-id="fd44d-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="fd44d-109">Il ripristino di uno snapshot sovrascrive tutti i file in un'app Web con i file contenuti nello snapshot.</span><span class="sxs-lookup"><span data-stu-id="fd44d-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="fd44d-110">Per ripristinare anche le impostazioni, usa il parametro RecoverConfiguration switch.</span><span class="sxs-lookup"><span data-stu-id="fd44d-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="fd44d-111">Uno snapshot da un'app Web può essere ripristinato in qualsiasi altra app Web nello stesso abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fd44d-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="fd44d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd44d-112">EXAMPLES</span></span>

### <span data-ttu-id="fd44d-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fd44d-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="fd44d-114">Ottiene lo snapshot più recente di un'app Web denominata "ContosoApp" con uno slot denominato "Staging" nel gruppo di risorse "default-Web-Westus".</span><span class="sxs-lookup"><span data-stu-id="fd44d-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="fd44d-115">Ripristina lo snapshot nello slot "ripristino" dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="fd44d-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="fd44d-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd44d-116">PARAMETERS</span></span>

### <span data-ttu-id="fd44d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd44d-117">-AsJob</span></span>
<span data-ttu-id="fd44d-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="fd44d-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd44d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd44d-119">-DefaultProfile</span></span>
<span data-ttu-id="fd44d-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fd44d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd44d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="fd44d-121">-Force</span></span>
<span data-ttu-id="fd44d-122">Consente di sovrascrivere l'app Web originale senza visualizzare un avviso.</span><span class="sxs-lookup"><span data-stu-id="fd44d-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd44d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd44d-123">-InputObject</span></span>
<span data-ttu-id="fd44d-124">Lo snapshot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="fd44d-124">The Azure Web App snapshot.</span></span>
```yaml
Type: AzureWebAppSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd44d-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd44d-125">-Name</span></span>
<span data-ttu-id="fd44d-126">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="fd44d-126">The name of the web app.</span></span>
```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd44d-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd44d-127">-RecoverConfiguration</span></span>
<span data-ttu-id="fd44d-128">Recupera la configurazione dell'app Web oltre ai file.</span><span class="sxs-lookup"><span data-stu-id="fd44d-128">Recover the web app's configuration in addition to files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd44d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd44d-129">-ResourceGroupName</span></span>
<span data-ttu-id="fd44d-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fd44d-130">The name of the resource group.</span></span>
```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd44d-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="fd44d-131">-Slot</span></span>
<span data-ttu-id="fd44d-132">Il nome dello slot Web App.</span><span class="sxs-lookup"><span data-stu-id="fd44d-132">The name of the web app slot.</span></span>
```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd44d-133">-Web App</span><span class="sxs-lookup"><span data-stu-id="fd44d-133">-WebApp</span></span>
<span data-ttu-id="fd44d-134">Oggetto app Web</span><span class="sxs-lookup"><span data-stu-id="fd44d-134">The web app object</span></span>
```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd44d-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fd44d-135">-Confirm</span></span>
<span data-ttu-id="fd44d-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd44d-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd44d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd44d-137">-WhatIf</span></span>
<span data-ttu-id="fd44d-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd44d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd44d-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd44d-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd44d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd44d-140">CommonParameters</span></span>
<span data-ttu-id="fd44d-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd44d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd44d-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd44d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd44d-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fd44d-143">INPUTS</span></span>

### <span data-ttu-id="fd44d-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fd44d-144">System.Management.Automation.SwitchParameter</span></span>
<span data-ttu-id="fd44d-145">Microsoft. Azure. Management. website. Models. Site System. String Microsoft. Azure. Commands. webapps. Cmdlets. BackupRestore. AzureWebAppSnapshot System. DateTime</span><span class="sxs-lookup"><span data-stu-id="fd44d-145">Microsoft.Azure.Management.WebSites.Models.Site System.String Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot System.DateTime</span></span>

## <span data-ttu-id="fd44d-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd44d-146">OUTPUTS</span></span>

### <span data-ttu-id="fd44d-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="fd44d-147">System.Object</span></span>

## <span data-ttu-id="fd44d-148">Note</span><span class="sxs-lookup"><span data-stu-id="fd44d-148">NOTES</span></span>

## <span data-ttu-id="fd44d-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd44d-149">RELATED LINKS</span></span>

