---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: a47f490ae77fc540f3e14708b19dade5ce4e7c3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514724"
---
# <span data-ttu-id="ad5bb-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ad5bb-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="ad5bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad5bb-102">SYNOPSIS</span></span>
<span data-ttu-id="ad5bb-103">Modifica un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="ad5bb-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad5bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad5bb-104">SYNTAX</span></span>

### <span data-ttu-id="ad5bb-105">S1</span><span class="sxs-lookup"><span data-stu-id="ad5bb-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-ContainerImageName <String>] [-ContainerRegistryUrl <String>]
 [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob]
 [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad5bb-106">S2</span><span class="sxs-lookup"><span data-stu-id="ad5bb-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad5bb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad5bb-107">DESCRIPTION</span></span>
<span data-ttu-id="ad5bb-108">Il cmdlet **set-AzureRmWebApp** imposta una Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ad5bb-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="ad5bb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad5bb-109">EXAMPLES</span></span>

### <span data-ttu-id="ad5bb-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ad5bb-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="ad5bb-111">Questo comando imposta HttpLoggingEnabled su true per l'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="ad5bb-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="ad5bb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad5bb-112">PARAMETERS</span></span>

### <span data-ttu-id="ad5bb-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ad5bb-113">-AppServicePlan</span></span>
<span data-ttu-id="ad5bb-114">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="ad5bb-114">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="ad5bb-115">-AppSettings</span></span>
<span data-ttu-id="ad5bb-116">HashTable delle impostazioni dell'app</span><span class="sxs-lookup"><span data-stu-id="ad5bb-116">App Settings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad5bb-117">-AsJob</span></span>
<span data-ttu-id="ad5bb-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ad5bb-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad5bb-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ad5bb-119">-AssignIdentity</span></span>
<span data-ttu-id="ad5bb-120">Abilitare/disabilitare MSI in un Web App o functionapp di Azure esistente</span><span class="sxs-lookup"><span data-stu-id="ad5bb-120">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="ad5bb-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="ad5bb-122">Nome dello slot di destinazione per lo scambio automatico</span><span class="sxs-lookup"><span data-stu-id="ad5bb-122">Destination slot name for auto swap</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="ad5bb-123">-ConnectionStrings</span></span>
<span data-ttu-id="ad5bb-124">HashTable stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="ad5bb-124">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="ad5bb-125">-ContainerImageName</span></span>
<span data-ttu-id="ad5bb-126">Nome immagine contenitore</span><span class="sxs-lookup"><span data-stu-id="ad5bb-126">Container Image Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="ad5bb-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="ad5bb-128">Password del registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="ad5bb-128">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="ad5bb-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="ad5bb-130">URL del server del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="ad5bb-130">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="ad5bb-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="ad5bb-132">Nome utente del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="ad5bb-132">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-133">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="ad5bb-133">-DefaultDocuments</span></span>
<span data-ttu-id="ad5bb-134">Matrice di stringhe documenti predefinita</span><span class="sxs-lookup"><span data-stu-id="ad5bb-134">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad5bb-135">-DefaultProfile</span></span>
<span data-ttu-id="ad5bb-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5bb-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad5bb-137">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="ad5bb-137">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="ad5bb-138">Errore di registrazione dettagliata delle funzionalità booleane</span><span class="sxs-lookup"><span data-stu-id="ad5bb-138">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-139">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="ad5bb-139">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="ad5bb-140">Abilita/Disabilita il webhook di distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="ad5bb-140">Enables/Disables container continuous deployment webhook</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-141">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="ad5bb-141">-HandlerMappings</span></span>
<span data-ttu-id="ad5bb-142">Interfaccia di mapping dei gestori</span><span class="sxs-lookup"><span data-stu-id="ad5bb-142">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: S1
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-143">-HostName</span><span class="sxs-lookup"><span data-stu-id="ad5bb-143">-HostNames</span></span>
<span data-ttu-id="ad5bb-144">Matrice di stringhe Web App HostNames</span><span class="sxs-lookup"><span data-stu-id="ad5bb-144">WebApp HostNames String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-145">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="ad5bb-145">-HttpLoggingEnabled</span></span>
<span data-ttu-id="ad5bb-146">HttpLoggingEnabled booleano</span><span class="sxs-lookup"><span data-stu-id="ad5bb-146">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-147">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="ad5bb-147">-HttpsOnly</span></span>
<span data-ttu-id="ad5bb-148">Abilitare/disabilitare il reindirizzamento di tutto il traffico a HTTPS in un Azure Web App o functionapp esistente</span><span class="sxs-lookup"><span data-stu-id="ad5bb-148">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-149">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="ad5bb-149">-ManagedPipelineMode</span></span>
<span data-ttu-id="ad5bb-150">Nome della modalità pipeline gestita</span><span class="sxs-lookup"><span data-stu-id="ad5bb-150">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad5bb-151">-Name</span></span>
<span data-ttu-id="ad5bb-152">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="ad5bb-152">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-153">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="ad5bb-153">-NetFrameworkVersion</span></span>
<span data-ttu-id="ad5bb-154">NET Framework</span><span class="sxs-lookup"><span data-stu-id="ad5bb-154">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-155">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="ad5bb-155">-NumberOfWorkers</span></span>
<span data-ttu-id="ad5bb-156">Numero di dipendenti da allocare</span><span class="sxs-lookup"><span data-stu-id="ad5bb-156">The number of workers to be allocated</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-157">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="ad5bb-157">-PhpVersion</span></span>
<span data-ttu-id="ad5bb-158">Versione php</span><span class="sxs-lookup"><span data-stu-id="ad5bb-158">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-159">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="ad5bb-159">-RequestTracingEnabled</span></span>
<span data-ttu-id="ad5bb-160">Richiesta di traccia attivata</span><span class="sxs-lookup"><span data-stu-id="ad5bb-160">Request Tracing Enabled</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad5bb-161">-ResourceGroupName</span></span>
<span data-ttu-id="ad5bb-162">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ad5bb-162">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-163">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="ad5bb-163">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="ad5bb-164">Usare il processo di lavoro a 32 bit Boolean</span><span class="sxs-lookup"><span data-stu-id="ad5bb-164">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-165">-Web App</span><span class="sxs-lookup"><span data-stu-id="ad5bb-165">-WebApp</span></span>
<span data-ttu-id="ad5bb-166">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="ad5bb-166">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-167">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="ad5bb-167">-WebSocketsEnabled</span></span>
<span data-ttu-id="ad5bb-168">WebSocketsEnabled booleano</span><span class="sxs-lookup"><span data-stu-id="ad5bb-168">WebSocketsEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5bb-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad5bb-169">CommonParameters</span></span>
<span data-ttu-id="ad5bb-170">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad5bb-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad5bb-171">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad5bb-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad5bb-172">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad5bb-172">INPUTS</span></span>

### <span data-ttu-id="ad5bb-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ad5bb-173">System.Int32</span></span>
<span data-ttu-id="ad5bb-174">Parametri: NumberOfWorkers (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ad5bb-174">Parameters: NumberOfWorkers (ByValue)</span></span>

### <span data-ttu-id="ad5bb-175">System. String</span><span class="sxs-lookup"><span data-stu-id="ad5bb-175">System.String</span></span>

### <span data-ttu-id="ad5bb-176">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="ad5bb-176">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="ad5bb-177">Parametri: Web App (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ad5bb-177">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="ad5bb-178">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad5bb-178">OUTPUTS</span></span>

### <span data-ttu-id="ad5bb-179">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="ad5bb-179">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="ad5bb-180">Note</span><span class="sxs-lookup"><span data-stu-id="ad5bb-180">NOTES</span></span>

## <span data-ttu-id="ad5bb-181">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad5bb-181">RELATED LINKS</span></span>

[<span data-ttu-id="ad5bb-182">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ad5bb-182">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="ad5bb-183">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ad5bb-183">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="ad5bb-184">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ad5bb-184">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="ad5bb-185">Riavviare-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ad5bb-185">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="ad5bb-186">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ad5bb-186">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="ad5bb-187">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ad5bb-187">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
