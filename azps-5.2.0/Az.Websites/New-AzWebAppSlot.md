---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 2228eb7562ed7a0ffa1c0098086c085985e45fee
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367093"
---
# <span data-ttu-id="8d289-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d289-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="8d289-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8d289-102">SYNOPSIS</span></span>
<span data-ttu-id="8d289-103">Crea uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="8d289-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="8d289-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8d289-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d289-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d289-105">DESCRIPTION</span></span>
<span data-ttu-id="8d289-106">Il cmdlet **New-AzWebAppSlot** crea uno slot di Azure Web App in un determinato gruppo di risorse che usa il piano di servizio app e il Data Center specificati.</span><span class="sxs-lookup"><span data-stu-id="8d289-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="8d289-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8d289-107">EXAMPLES</span></span>

### <span data-ttu-id="8d289-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8d289-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="8d289-109">Questo comando crea uno slot denominato Slot001 in un nome di app Web esistente ContosoSite nel gruppo di risorse esistente denominato Default-Web-Westus nel Data Center West US.</span><span class="sxs-lookup"><span data-stu-id="8d289-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="8d289-110">Il comando usa un piano di servizio app esistente denominato ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="8d289-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="8d289-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8d289-111">PARAMETERS</span></span>

### <span data-ttu-id="8d289-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8d289-112">-AppServicePlan</span></span>
<span data-ttu-id="8d289-113">Nome piano servizio app o ID piano servizio app. Se il piano di servizio slot e app si trova in gruppi di risorse diversi, usare l'ID anziché il nome.</span><span class="sxs-lookup"><span data-stu-id="8d289-113">App Service Plan Name or App Service Plan Id. If the Slot and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="8d289-114">L'ID piano di servizio app può essere recuperato usando: $asp = Get-AzAppServicePlan-ResourceGroup myRG-Name MyWebapp $asp. ID restituisce l'ID del piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="8d289-114">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>

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

### <span data-ttu-id="8d289-115">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="8d289-115">-AppSettingsOverrides</span></span>
<span data-ttu-id="8d289-116">Le impostazioni dell'app vengono sostituite da Hashtable</span><span class="sxs-lookup"><span data-stu-id="8d289-116">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="8d289-117">-AseName</span><span class="sxs-lookup"><span data-stu-id="8d289-117">-AseName</span></span>
<span data-ttu-id="8d289-118">Nome ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="8d289-118">App Service Environment Name</span></span>

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

### <span data-ttu-id="8d289-119">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d289-119">-AseResourceGroupName</span></span>
<span data-ttu-id="8d289-120">Nome del gruppo risorse ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="8d289-120">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="8d289-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d289-121">-AsJob</span></span>
<span data-ttu-id="8d289-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8d289-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8d289-123">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="8d289-123">-ContainerImageName</span></span>
<span data-ttu-id="8d289-124">Nome immagine contenitore e tag facoltativo, ad esempio (immagine: Tag)</span><span class="sxs-lookup"><span data-stu-id="8d289-124">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="8d289-125">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="8d289-125">-ContainerRegistryPassword</span></span>
<span data-ttu-id="8d289-126">Password del registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="8d289-126">Private Container Registry Password</span></span>

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

### <span data-ttu-id="8d289-127">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="8d289-127">-ContainerRegistryUrl</span></span>
<span data-ttu-id="8d289-128">URL del server del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="8d289-128">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="8d289-129">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="8d289-129">-ContainerRegistryUser</span></span>
<span data-ttu-id="8d289-130">Nome utente del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="8d289-130">Private Container Registry Username</span></span>

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

### <span data-ttu-id="8d289-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d289-131">-DefaultProfile</span></span>
<span data-ttu-id="8d289-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8d289-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d289-133">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="8d289-133">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="8d289-134">Abilita/Disabilita il webhook di distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="8d289-134">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="8d289-135">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="8d289-135">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="8d289-136">Opzione Ignora nomi host personalizzati</span><span class="sxs-lookup"><span data-stu-id="8d289-136">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="8d289-137">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="8d289-137">-IgnoreSourceControl</span></span>
<span data-ttu-id="8d289-138">Opzione Ignora controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="8d289-138">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="8d289-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="8d289-139">-Name</span></span>
<span data-ttu-id="8d289-140">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="8d289-140">Webapp Name</span></span>

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

### <span data-ttu-id="8d289-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d289-141">-ResourceGroupName</span></span>
<span data-ttu-id="8d289-142">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="8d289-142">Resource Group Name</span></span>

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

### <span data-ttu-id="8d289-143">-Slot</span><span class="sxs-lookup"><span data-stu-id="8d289-143">-Slot</span></span>
<span data-ttu-id="8d289-144">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="8d289-144">Webapp Slot Name</span></span>

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

### <span data-ttu-id="8d289-145">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="8d289-145">-SourceWebApp</span></span>
<span data-ttu-id="8d289-146">Oggetto Web App di origine</span><span class="sxs-lookup"><span data-stu-id="8d289-146">Source WebApp Object</span></span>

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

### <span data-ttu-id="8d289-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d289-147">CommonParameters</span></span>
<span data-ttu-id="8d289-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d289-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d289-149">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d289-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d289-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8d289-150">INPUTS</span></span>

### <span data-ttu-id="8d289-151">System. String</span><span class="sxs-lookup"><span data-stu-id="8d289-151">System.String</span></span>

### <span data-ttu-id="8d289-152">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="8d289-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8d289-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8d289-153">OUTPUTS</span></span>

### <span data-ttu-id="8d289-154">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="8d289-154">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8d289-155">Note</span><span class="sxs-lookup"><span data-stu-id="8d289-155">NOTES</span></span>

## <span data-ttu-id="8d289-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8d289-156">RELATED LINKS</span></span>

[<span data-ttu-id="8d289-157">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d289-157">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="8d289-158">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d289-158">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="8d289-159">Riavviare-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d289-159">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="8d289-160">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d289-160">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="8d289-161">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d289-161">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="8d289-162">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d289-162">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="8d289-163">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8d289-163">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="8d289-164">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8d289-164">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
