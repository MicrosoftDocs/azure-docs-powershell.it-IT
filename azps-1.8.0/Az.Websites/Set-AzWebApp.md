---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 7fb1118d612aae7cf5495f0743550510088e5dbe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676256"
---
# <span data-ttu-id="40690-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="40690-101">Set-AzWebApp</span></span>



## <span data-ttu-id="40690-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="40690-102">SYNOPSIS</span></span>

<span data-ttu-id="40690-103">Modifica un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="40690-103">Modifies an Azure Web App.</span></span>



## <span data-ttu-id="40690-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40690-104">SYNTAX</span></span>



### <span data-ttu-id="40690-105">S1</span><span class="sxs-lookup"><span data-stu-id="40690-105">S1</span></span>

```

Set-AzWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>] [[-NetFrameworkVersion] <String>]

 [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>] [[-HttpLoggingEnabled] <Boolean>]

 [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>] [[-ConnectionStrings] <Hashtable>]

 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]

 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]

 [[-AutoSwapSlotName] <String>] [-ContainerImageName <String>] [-ContainerRegistryUrl <String>]

 [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]

 [-EnableContainerContinuousDeployment <Boolean>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob]

 [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>] [-AzureStoragePath <WebAppAzureStoragePath[]>]

 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]

```



### <span data-ttu-id="40690-106">S2</span><span class="sxs-lookup"><span data-stu-id="40690-106">S2</span></span>

```

Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]

 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]

```



## <span data-ttu-id="40690-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40690-107">DESCRIPTION</span></span>

<span data-ttu-id="40690-108">Il cmdlet **set-AzWebApp** imposta una Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="40690-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>



## <span data-ttu-id="40690-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40690-109">EXAMPLES</span></span>



### <span data-ttu-id="40690-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="40690-110">Example 1</span></span>

```

PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"

```



<span data-ttu-id="40690-111">Questo comando modifica il piano Appservice associato all'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="40690-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="40690-112">Usare il collegamento per altre informazioni sulla modifica del piano Appservice e dei vincoli associati.</span><span class="sxs-lookup"><span data-stu-id="40690-112">Use the link to learm more about changing the appservice plan and constraints associated with it.</span></span>

https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan


### <span data-ttu-id="40690-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="40690-113">Example 2</span></span>

```

PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true

```



<span data-ttu-id="40690-114">Questo comando imposta HttpLoggingEnabled su true per l'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="40690-114">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>



## <span data-ttu-id="40690-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="40690-115">PARAMETERS</span></span>



### <span data-ttu-id="40690-116">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="40690-116">-AppServicePlan</span></span>

<span data-ttu-id="40690-117">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="40690-117">App Service Plan Name</span></span>



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



### <span data-ttu-id="40690-118">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="40690-118">-AppSettings</span></span>

<span data-ttu-id="40690-119">HashTable delle impostazioni dell'app</span><span class="sxs-lookup"><span data-stu-id="40690-119">App Settings HashTable</span></span>



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



### <span data-ttu-id="40690-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40690-120">-AsJob</span></span>

<span data-ttu-id="40690-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="40690-121">Run cmdlet in the background</span></span>



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



### <span data-ttu-id="40690-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="40690-122">-AssignIdentity</span></span>

<span data-ttu-id="40690-123">Abilitare/disabilitare MSI in un Web App o functionapp di Azure esistente</span><span class="sxs-lookup"><span data-stu-id="40690-123">Enable/disable MSI on an existing azure webapp or functionapp</span></span>



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



### <span data-ttu-id="40690-124">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="40690-124">-AutoSwapSlotName</span></span>

<span data-ttu-id="40690-125">Nome dello slot di destinazione per lo scambio automatico</span><span class="sxs-lookup"><span data-stu-id="40690-125">Destination slot name for auto swap</span></span>



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



### <span data-ttu-id="40690-126">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="40690-126">-AzureStoragePath</span></span>

<span data-ttu-id="40690-127">Spazio di archiviazione di Azure da montare all'interno di un'app Web per container.</span><span class="sxs-lookup"><span data-stu-id="40690-127">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="40690-128">Usare New-AzureRmWebAppAzureStoragePath per crearlo</span><span class="sxs-lookup"><span data-stu-id="40690-128">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>



```yaml

Type: Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath[]

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="40690-129">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="40690-129">-ConnectionStrings</span></span>

<span data-ttu-id="40690-130">HashTable stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="40690-130">Connection Strings HashTable</span></span>



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



### <span data-ttu-id="40690-131">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="40690-131">-ContainerImageName</span></span>

<span data-ttu-id="40690-132">Nome immagine contenitore</span><span class="sxs-lookup"><span data-stu-id="40690-132">Container Image Name</span></span>



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



### <span data-ttu-id="40690-133">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="40690-133">-ContainerRegistryPassword</span></span>

<span data-ttu-id="40690-134">Password del registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="40690-134">Private Container Registry Password</span></span>



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



### <span data-ttu-id="40690-135">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="40690-135">-ContainerRegistryUrl</span></span>

<span data-ttu-id="40690-136">URL del server del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="40690-136">Private Container Registry Server Url</span></span>



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



### <span data-ttu-id="40690-137">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="40690-137">-ContainerRegistryUser</span></span>

<span data-ttu-id="40690-138">Nome utente del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="40690-138">Private Container Registry Username</span></span>



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



### <span data-ttu-id="40690-139">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="40690-139">-DefaultDocuments</span></span>

<span data-ttu-id="40690-140">Matrice di stringhe documenti predefinita</span><span class="sxs-lookup"><span data-stu-id="40690-140">Default Documents String Array</span></span>



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



### <span data-ttu-id="40690-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40690-141">-DefaultProfile</span></span>

<span data-ttu-id="40690-142">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="40690-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>



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



### <span data-ttu-id="40690-143">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="40690-143">-DetailedErrorLoggingEnabled</span></span>

<span data-ttu-id="40690-144">Errore di registrazione dettagliata delle funzionalità booleane</span><span class="sxs-lookup"><span data-stu-id="40690-144">Detailed Error Logging Enabled Boolean</span></span>



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



### <span data-ttu-id="40690-145">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="40690-145">-EnableContainerContinuousDeployment</span></span>

<span data-ttu-id="40690-146">Abilita/Disabilita il webhook di distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="40690-146">Enables/Disables container continuous deployment webhook</span></span>



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



### <span data-ttu-id="40690-147">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="40690-147">-HandlerMappings</span></span>

<span data-ttu-id="40690-148">Interfaccia di mapping dei gestori</span><span class="sxs-lookup"><span data-stu-id="40690-148">Handler Mappings IList</span></span>



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



### <span data-ttu-id="40690-149">-HostName</span><span class="sxs-lookup"><span data-stu-id="40690-149">-HostNames</span></span>

<span data-ttu-id="40690-150">Matrice di stringhe Web App HostNames</span><span class="sxs-lookup"><span data-stu-id="40690-150">WebApp HostNames String Array</span></span>



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



### <span data-ttu-id="40690-151">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="40690-151">-HttpLoggingEnabled</span></span>

<span data-ttu-id="40690-152">HttpLoggingEnabled booleano</span><span class="sxs-lookup"><span data-stu-id="40690-152">HttpLoggingEnabled Boolean</span></span>



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



### <span data-ttu-id="40690-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="40690-153">-HttpsOnly</span></span>

<span data-ttu-id="40690-154">Abilitare/disabilitare il reindirizzamento di tutto il traffico a HTTPS in un Azure Web App o functionapp esistente</span><span class="sxs-lookup"><span data-stu-id="40690-154">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>



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



### <span data-ttu-id="40690-155">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="40690-155">-ManagedPipelineMode</span></span>

<span data-ttu-id="40690-156">Nome della modalità pipeline gestita</span><span class="sxs-lookup"><span data-stu-id="40690-156">Managed Pipeline Mode Name</span></span>



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



### <span data-ttu-id="40690-157">-Nome</span><span class="sxs-lookup"><span data-stu-id="40690-157">-Name</span></span>

<span data-ttu-id="40690-158">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="40690-158">WebApp Name</span></span>



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



### <span data-ttu-id="40690-159">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="40690-159">-NetFrameworkVersion</span></span>

<span data-ttu-id="40690-160">NET Framework</span><span class="sxs-lookup"><span data-stu-id="40690-160">Net Framework Version</span></span>



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



### <span data-ttu-id="40690-161">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="40690-161">-NumberOfWorkers</span></span>

<span data-ttu-id="40690-162">Numero di dipendenti da allocare</span><span class="sxs-lookup"><span data-stu-id="40690-162">The number of workers to be allocated</span></span>



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



### <span data-ttu-id="40690-163">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="40690-163">-PhpVersion</span></span>

<span data-ttu-id="40690-164">Versione php</span><span class="sxs-lookup"><span data-stu-id="40690-164">Php Version</span></span>



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



### <span data-ttu-id="40690-165">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="40690-165">-RequestTracingEnabled</span></span>

<span data-ttu-id="40690-166">Richiesta di traccia attivata</span><span class="sxs-lookup"><span data-stu-id="40690-166">Request Tracing Enabled</span></span>



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



### <span data-ttu-id="40690-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40690-167">-ResourceGroupName</span></span>

<span data-ttu-id="40690-168">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="40690-168">Resource Group Name</span></span>



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



### <span data-ttu-id="40690-169">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="40690-169">-Use32BitWorkerProcess</span></span>

<span data-ttu-id="40690-170">Usare il processo di lavoro a 32 bit Boolean</span><span class="sxs-lookup"><span data-stu-id="40690-170">Use 32-bit Worker Process Boolean</span></span>



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



### <span data-ttu-id="40690-171">-Web App</span><span class="sxs-lookup"><span data-stu-id="40690-171">-WebApp</span></span>

<span data-ttu-id="40690-172">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="40690-172">WebApp Object</span></span>



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



### <span data-ttu-id="40690-173">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="40690-173">-WebSocketsEnabled</span></span>

<span data-ttu-id="40690-174">WebSocketsEnabled booleano</span><span class="sxs-lookup"><span data-stu-id="40690-174">WebSocketsEnabled Boolean</span></span>



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



### <span data-ttu-id="40690-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40690-175">CommonParameters</span></span>

<span data-ttu-id="40690-176">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40690-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40690-177">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40690-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>



## <span data-ttu-id="40690-178">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="40690-178">INPUTS</span></span>



### <span data-ttu-id="40690-179">System. Int32</span><span class="sxs-lookup"><span data-stu-id="40690-179">System.Int32</span></span>



### <span data-ttu-id="40690-180">System. String</span><span class="sxs-lookup"><span data-stu-id="40690-180">System.String</span></span>



### <span data-ttu-id="40690-181">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="40690-181">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>



## <span data-ttu-id="40690-182">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40690-182">OUTPUTS</span></span>



### <span data-ttu-id="40690-183">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="40690-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>



## <span data-ttu-id="40690-184">Note</span><span class="sxs-lookup"><span data-stu-id="40690-184">NOTES</span></span>



## <span data-ttu-id="40690-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40690-185">RELATED LINKS</span></span>



[<span data-ttu-id="40690-186">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="40690-186">Get-AzWebApp</span></span>](./Get-AzWebApp.md)



[<span data-ttu-id="40690-187">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="40690-187">New-AzWebApp</span></span>](./New-AzWebApp.md)



[<span data-ttu-id="40690-188">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="40690-188">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)



[<span data-ttu-id="40690-189">Riavviare-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="40690-189">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)



[<span data-ttu-id="40690-190">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="40690-190">Start-AzWebApp</span></span>](./Start-AzWebApp.md)



[<span data-ttu-id="40690-191">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="40690-191">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

