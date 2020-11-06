---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
ms.openlocfilehash: 6c7fbd4512bfac7a369f21f85803653c6f7c9628
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520558"
---
# <span data-ttu-id="44514-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44514-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="44514-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="44514-102">SYNOPSIS</span></span>
<span data-ttu-id="44514-103">Crea uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="44514-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44514-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44514-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44514-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44514-105">DESCRIPTION</span></span>
<span data-ttu-id="44514-106">Il cmdlet **New-AzureRmWebAppSlot** crea uno slot di Azure Web App in un determinato gruppo di risorse che usa il piano di servizio app e il Data Center specificati.</span><span class="sxs-lookup"><span data-stu-id="44514-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="44514-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44514-107">EXAMPLES</span></span>

### <span data-ttu-id="44514-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="44514-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="44514-109">Questo comando crea uno slot denominato Slot001 in un nome di app Web esistente ContosoSite nel gruppo di risorse esistente denominato Default-Web-Westus nel Data Center West US.</span><span class="sxs-lookup"><span data-stu-id="44514-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="44514-110">Il comando usa un piano di servizio app esistente denominato ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="44514-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="44514-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="44514-111">PARAMETERS</span></span>

### <span data-ttu-id="44514-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="44514-112">-AppServicePlan</span></span>
<span data-ttu-id="44514-113">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="44514-113">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44514-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="44514-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="44514-115">Le impostazioni dell'app vengono sostituite da Hashtable</span><span class="sxs-lookup"><span data-stu-id="44514-115">App Settings Overrides Hashtable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44514-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="44514-116">-AseName</span></span>
<span data-ttu-id="44514-117">Nome ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="44514-117">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44514-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44514-118">-AseResourceGroupName</span></span>
<span data-ttu-id="44514-119">Nome del gruppo risorse ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="44514-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44514-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44514-120">-AsJob</span></span>
<span data-ttu-id="44514-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="44514-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44514-122">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="44514-122">-ContainerImageName</span></span>
<span data-ttu-id="44514-123">Nome immagine contenitore e tag facoltativo, ad esempio (immagine: Tag)</span><span class="sxs-lookup"><span data-stu-id="44514-123">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="44514-124">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="44514-124">-ContainerRegistryPassword</span></span>
<span data-ttu-id="44514-125">Password del registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="44514-125">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44514-126">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="44514-126">-ContainerRegistryUrl</span></span>
<span data-ttu-id="44514-127">URL del server del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="44514-127">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="44514-128">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="44514-128">-ContainerRegistryUser</span></span>
<span data-ttu-id="44514-129">Nome utente del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="44514-129">Private Container Registry Username</span></span>

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

### <span data-ttu-id="44514-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44514-130">-DefaultProfile</span></span>
<span data-ttu-id="44514-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="44514-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44514-132">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="44514-132">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="44514-133">Abilita/Disabilita il webhook di distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="44514-133">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="44514-134">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="44514-134">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="44514-135">Opzione Ignora nomi host personalizzati</span><span class="sxs-lookup"><span data-stu-id="44514-135">Ignore Custom HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44514-136">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="44514-136">-IgnoreSourceControl</span></span>
<span data-ttu-id="44514-137">Opzione Ignora controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="44514-137">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44514-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="44514-138">-Name</span></span>
<span data-ttu-id="44514-139">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="44514-139">Webapp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44514-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44514-140">-ResourceGroupName</span></span>
<span data-ttu-id="44514-141">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="44514-141">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44514-142">-Slot</span><span class="sxs-lookup"><span data-stu-id="44514-142">-Slot</span></span>
<span data-ttu-id="44514-143">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="44514-143">Webapp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44514-144">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="44514-144">-SourceWebApp</span></span>
<span data-ttu-id="44514-145">Oggetto Web App di origine</span><span class="sxs-lookup"><span data-stu-id="44514-145">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44514-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44514-146">CommonParameters</span></span>
<span data-ttu-id="44514-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44514-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44514-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44514-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44514-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="44514-149">INPUTS</span></span>

### <span data-ttu-id="44514-150">System. String</span><span class="sxs-lookup"><span data-stu-id="44514-150">System.String</span></span>

### <span data-ttu-id="44514-151">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="44514-151">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="44514-152">Parametri: SourceWebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="44514-152">Parameters: SourceWebApp (ByValue)</span></span>

## <span data-ttu-id="44514-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44514-153">OUTPUTS</span></span>

### <span data-ttu-id="44514-154">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="44514-154">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="44514-155">Note</span><span class="sxs-lookup"><span data-stu-id="44514-155">NOTES</span></span>

## <span data-ttu-id="44514-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44514-156">RELATED LINKS</span></span>

[<span data-ttu-id="44514-157">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44514-157">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="44514-158">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44514-158">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="44514-159">Riavviare-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44514-159">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="44514-160">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44514-160">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="44514-161">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44514-161">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="44514-162">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44514-162">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="44514-163">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="44514-163">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="44514-164">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="44514-164">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
