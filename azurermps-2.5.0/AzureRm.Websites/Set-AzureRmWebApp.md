---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: d722c378e246fa175741c91092d99415275f094e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866164"
---
# <span data-ttu-id="3eece-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3eece-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="3eece-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3eece-102">SYNOPSIS</span></span>
<span data-ttu-id="3eece-103">Modifica un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="3eece-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3eece-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3eece-104">SYNTAX</span></span>

### <span data-ttu-id="3eece-105">S1</span><span class="sxs-lookup"><span data-stu-id="3eece-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob] [[-AssignIdentity] <Boolean>]
 [[-HttpsOnly] <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3eece-106">S2</span><span class="sxs-lookup"><span data-stu-id="3eece-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3eece-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3eece-107">DESCRIPTION</span></span>
<span data-ttu-id="3eece-108">Il cmdlet **set-AzureRmWebApp** imposta una Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="3eece-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="3eece-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3eece-109">EXAMPLES</span></span>

### <span data-ttu-id="3eece-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3eece-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="3eece-111">Questo comando imposta HttpLoggingEnabled su true per l'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="3eece-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="3eece-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3eece-112">PARAMETERS</span></span>

### <span data-ttu-id="3eece-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3eece-113">-AppServicePlan</span></span>
<span data-ttu-id="3eece-114">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="3eece-114">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eece-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="3eece-115">-AppSettings</span></span>
<span data-ttu-id="3eece-116">HashTable delle impostazioni dell'app</span><span class="sxs-lookup"><span data-stu-id="3eece-116">App Settings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eece-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3eece-117">-AsJob</span></span>
<span data-ttu-id="3eece-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3eece-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3eece-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="3eece-119">-AssignIdentity</span></span>
<span data-ttu-id="3eece-120">Abilitare/disabilitare MSI in un Web App o functionapp di Azure esistente [PREVIEW]</span><span class="sxs-lookup"><span data-stu-id="3eece-120">Enable/disable MSI on an existing azure webapp or functionapp [PREVIEW]</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eece-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="3eece-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="3eece-122">Nome dello slot di destinazione per lo scambio automatico</span><span class="sxs-lookup"><span data-stu-id="3eece-122">Destination slot name for auto swap</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eece-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="3eece-123">-ConnectionStrings</span></span>
<span data-ttu-id="3eece-124">HashTable stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="3eece-124">Connection Strings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eece-125">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="3eece-125">-DefaultDocuments</span></span>
<span data-ttu-id="3eece-126">Matrice di stringhe documenti predefinita</span><span class="sxs-lookup"><span data-stu-id="3eece-126">Default Documents String Array</span></span>

```yaml
Type: String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eece-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eece-127">-DefaultProfile</span></span>
<span data-ttu-id="3eece-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3eece-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3eece-129">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="3eece-129">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="3eece-130">Errore di registrazione dettagliata delle funzionalità booleane</span><span class="sxs-lookup"><span data-stu-id="3eece-130">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eece-131">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="3eece-131">-HandlerMappings</span></span>
<span data-ttu-id="3eece-132">Interfaccia di mapping dei gestori</span><span class="sxs-lookup"><span data-stu-id="3eece-132">Handler Mappings IList</span></span>

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

### <span data-ttu-id="3eece-133">-HostName</span><span class="sxs-lookup"><span data-stu-id="3eece-133">-HostNames</span></span>
<span data-ttu-id="3eece-134">Matrice di stringhe Web App HostNames</span><span class="sxs-lookup"><span data-stu-id="3eece-134">WebApp HostNames String Array</span></span>

```yaml
Type: String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eece-135">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="3eece-135">-HttpLoggingEnabled</span></span>
<span data-ttu-id="3eece-136">HttpLoggingEnabled booleano</span><span class="sxs-lookup"><span data-stu-id="3eece-136">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eece-137">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="3eece-137">-HttpsOnly</span></span>
<span data-ttu-id="3eece-138">Abilitare/disabilitare il reindirizzamento di tutto il traffico a HTTPS in un Azure Web App o functionapp esistente</span><span class="sxs-lookup"><span data-stu-id="3eece-138">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eece-139">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="3eece-139">-ManagedPipelineMode</span></span>
<span data-ttu-id="3eece-140">Nome della modalità pipeline gestita</span><span class="sxs-lookup"><span data-stu-id="3eece-140">Managed Pipeline Mode Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eece-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="3eece-141">-Name</span></span>
<span data-ttu-id="3eece-142">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="3eece-142">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3eece-143">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="3eece-143">-NetFrameworkVersion</span></span>
<span data-ttu-id="3eece-144">NET Framework</span><span class="sxs-lookup"><span data-stu-id="3eece-144">Net Framework Version</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eece-145">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="3eece-145">-NumberOfWorkers</span></span>
<span data-ttu-id="3eece-146">Numero di dipendenti da allocare</span><span class="sxs-lookup"><span data-stu-id="3eece-146">The number of workers to be allocated</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3eece-147">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="3eece-147">-PhpVersion</span></span>
<span data-ttu-id="3eece-148">Versione php</span><span class="sxs-lookup"><span data-stu-id="3eece-148">Php Version</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eece-149">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="3eece-149">-RequestTracingEnabled</span></span>
<span data-ttu-id="3eece-150">Richiesta di traccia attivata</span><span class="sxs-lookup"><span data-stu-id="3eece-150">Request Tracing Enabled</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eece-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eece-151">-ResourceGroupName</span></span>
<span data-ttu-id="3eece-152">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="3eece-152">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eece-153">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="3eece-153">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="3eece-154">Usare il processo di lavoro a 32 bit Boolean</span><span class="sxs-lookup"><span data-stu-id="3eece-154">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eece-155">-Web App</span><span class="sxs-lookup"><span data-stu-id="3eece-155">-WebApp</span></span>
<span data-ttu-id="3eece-156">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="3eece-156">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3eece-157">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="3eece-157">-WebSocketsEnabled</span></span>
<span data-ttu-id="3eece-158">WebSocketsEnabled booleano</span><span class="sxs-lookup"><span data-stu-id="3eece-158">WebSocketsEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eece-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eece-159">CommonParameters</span></span>
<span data-ttu-id="3eece-160">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eece-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eece-161">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eece-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eece-162">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3eece-162">INPUTS</span></span>

### <span data-ttu-id="3eece-163">Int32</span><span class="sxs-lookup"><span data-stu-id="3eece-163">Int32</span></span>
<span data-ttu-id="3eece-164">Il parametro "NumberOfWorkers" accetta il valore di tipo "Int32" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3eece-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="3eece-165">Sito</span><span class="sxs-lookup"><span data-stu-id="3eece-165">Site</span></span>
<span data-ttu-id="3eece-166">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3eece-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="3eece-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3eece-167">OUTPUTS</span></span>

## <span data-ttu-id="3eece-168">Note</span><span class="sxs-lookup"><span data-stu-id="3eece-168">NOTES</span></span>

## <span data-ttu-id="3eece-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3eece-169">RELATED LINKS</span></span>

[<span data-ttu-id="3eece-170">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3eece-170">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="3eece-171">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3eece-171">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="3eece-172">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3eece-172">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="3eece-173">Riavviare-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3eece-173">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="3eece-174">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3eece-174">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="3eece-175">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3eece-175">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
