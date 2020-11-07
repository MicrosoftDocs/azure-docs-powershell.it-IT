---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 941de31e1733bd591507176216e30f9e1510f706
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676283"
---
# <span data-ttu-id="36405-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="36405-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="36405-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36405-102">SYNOPSIS</span></span>
<span data-ttu-id="36405-103">Crea uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="36405-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="36405-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36405-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36405-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36405-105">DESCRIPTION</span></span>
<span data-ttu-id="36405-106">Il cmdlet **New-AzWebAppSlot** crea uno slot di Azure Web App in un determinato gruppo di risorse che usa il piano di servizio app e il Data Center specificati.</span><span class="sxs-lookup"><span data-stu-id="36405-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="36405-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36405-107">EXAMPLES</span></span>

### <span data-ttu-id="36405-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="36405-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="36405-109">Questo comando crea uno slot denominato Slot001 in un nome di app Web esistente ContosoSite nel gruppo di risorse esistente denominato Default-Web-Westus nel Data Center West US.</span><span class="sxs-lookup"><span data-stu-id="36405-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="36405-110">Il comando usa un piano di servizio app esistente denominato ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="36405-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="36405-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36405-111">PARAMETERS</span></span>

### <span data-ttu-id="36405-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="36405-112">-AppServicePlan</span></span>
<span data-ttu-id="36405-113">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="36405-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="36405-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="36405-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="36405-115">Le impostazioni dell'app vengono sostituite da Hashtable</span><span class="sxs-lookup"><span data-stu-id="36405-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="36405-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="36405-116">-AseName</span></span>
<span data-ttu-id="36405-117">Nome ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="36405-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="36405-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36405-118">-AseResourceGroupName</span></span>
<span data-ttu-id="36405-119">Nome del gruppo risorse ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="36405-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="36405-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36405-120">-AsJob</span></span>
<span data-ttu-id="36405-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="36405-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36405-122">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="36405-122">-ContainerImageName</span></span>
<span data-ttu-id="36405-123">Nome immagine contenitore e tag facoltativo, ad esempio (immagine: Tag)</span><span class="sxs-lookup"><span data-stu-id="36405-123">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="36405-124">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="36405-124">-ContainerRegistryPassword</span></span>
<span data-ttu-id="36405-125">Password del registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="36405-125">Private Container Registry Password</span></span>

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

### <span data-ttu-id="36405-126">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="36405-126">-ContainerRegistryUrl</span></span>
<span data-ttu-id="36405-127">URL del server del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="36405-127">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="36405-128">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="36405-128">-ContainerRegistryUser</span></span>
<span data-ttu-id="36405-129">Nome utente del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="36405-129">Private Container Registry Username</span></span>

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

### <span data-ttu-id="36405-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36405-130">-DefaultProfile</span></span>
<span data-ttu-id="36405-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36405-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36405-132">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="36405-132">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="36405-133">Abilita/Disabilita il webhook di distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="36405-133">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="36405-134">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="36405-134">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="36405-135">Opzione Ignora nomi host personalizzati</span><span class="sxs-lookup"><span data-stu-id="36405-135">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="36405-136">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="36405-136">-IgnoreSourceControl</span></span>
<span data-ttu-id="36405-137">Opzione Ignora controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="36405-137">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="36405-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="36405-138">-Name</span></span>
<span data-ttu-id="36405-139">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="36405-139">Webapp Name</span></span>

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

### <span data-ttu-id="36405-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36405-140">-ResourceGroupName</span></span>
<span data-ttu-id="36405-141">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="36405-141">Resource Group Name</span></span>

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

### <span data-ttu-id="36405-142">-Slot</span><span class="sxs-lookup"><span data-stu-id="36405-142">-Slot</span></span>
<span data-ttu-id="36405-143">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="36405-143">Webapp Slot Name</span></span>

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

### <span data-ttu-id="36405-144">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="36405-144">-SourceWebApp</span></span>
<span data-ttu-id="36405-145">Oggetto Web App di origine</span><span class="sxs-lookup"><span data-stu-id="36405-145">Source WebApp Object</span></span>

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

### <span data-ttu-id="36405-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36405-146">CommonParameters</span></span>
<span data-ttu-id="36405-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36405-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36405-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36405-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36405-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36405-149">INPUTS</span></span>

### <span data-ttu-id="36405-150">System. String</span><span class="sxs-lookup"><span data-stu-id="36405-150">System.String</span></span>

### <span data-ttu-id="36405-151">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="36405-151">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="36405-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36405-152">OUTPUTS</span></span>

### <span data-ttu-id="36405-153">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="36405-153">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="36405-154">Note</span><span class="sxs-lookup"><span data-stu-id="36405-154">NOTES</span></span>

## <span data-ttu-id="36405-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36405-155">RELATED LINKS</span></span>

[<span data-ttu-id="36405-156">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="36405-156">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="36405-157">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="36405-157">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="36405-158">Riavviare-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="36405-158">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="36405-159">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="36405-159">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="36405-160">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="36405-160">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="36405-161">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="36405-161">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="36405-162">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="36405-162">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="36405-163">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="36405-163">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
