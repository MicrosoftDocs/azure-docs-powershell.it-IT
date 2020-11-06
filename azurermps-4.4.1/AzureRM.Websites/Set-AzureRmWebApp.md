---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: 0f8008a2b567bb2cb2b67755d2ea5bb586f0c115
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511211"
---
# <span data-ttu-id="69d0b-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="69d0b-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="69d0b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69d0b-102">SYNOPSIS</span></span>
<span data-ttu-id="69d0b-103">Modifica un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="69d0b-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69d0b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69d0b-104">SYNTAX</span></span>

### <span data-ttu-id="69d0b-105">S1</span><span class="sxs-lookup"><span data-stu-id="69d0b-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69d0b-106">S2</span><span class="sxs-lookup"><span data-stu-id="69d0b-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69d0b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69d0b-107">DESCRIPTION</span></span>
<span data-ttu-id="69d0b-108">Il cmdlet **set-AzureRmWebApp** imposta una Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="69d0b-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="69d0b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69d0b-109">EXAMPLES</span></span>

### <span data-ttu-id="69d0b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="69d0b-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="69d0b-111">Questo comando imposta HttpLoggingEnabled su true per l'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="69d0b-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="69d0b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69d0b-112">PARAMETERS</span></span>

### <span data-ttu-id="69d0b-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="69d0b-113">-AppServicePlan</span></span>
<span data-ttu-id="69d0b-114">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="69d0b-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="69d0b-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="69d0b-115">-AppSettings</span></span>
<span data-ttu-id="69d0b-116">HashTable delle impostazioni dell'app</span><span class="sxs-lookup"><span data-stu-id="69d0b-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="69d0b-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="69d0b-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="69d0b-118">Nome dello slot di destinazione per lo scambio automatico</span><span class="sxs-lookup"><span data-stu-id="69d0b-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="69d0b-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="69d0b-119">-ConnectionStrings</span></span>
<span data-ttu-id="69d0b-120">HashTable stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="69d0b-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="69d0b-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="69d0b-121">-DefaultDocuments</span></span>
<span data-ttu-id="69d0b-122">Matrice di stringhe documenti predefinita</span><span class="sxs-lookup"><span data-stu-id="69d0b-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="69d0b-123">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="69d0b-123">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="69d0b-124">Errore di registrazione dettagliata delle funzionalità booleane</span><span class="sxs-lookup"><span data-stu-id="69d0b-124">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="69d0b-125">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="69d0b-125">-HandlerMappings</span></span>
<span data-ttu-id="69d0b-126">Interfaccia di mapping dei gestori</span><span class="sxs-lookup"><span data-stu-id="69d0b-126">Handler Mappings IList</span></span>

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

### <span data-ttu-id="69d0b-127">-HostName</span><span class="sxs-lookup"><span data-stu-id="69d0b-127">-HostNames</span></span>
<span data-ttu-id="69d0b-128">Matrice di stringhe Web App HostNames</span><span class="sxs-lookup"><span data-stu-id="69d0b-128">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="69d0b-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="69d0b-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="69d0b-130">HttpLoggingEnabled booleano</span><span class="sxs-lookup"><span data-stu-id="69d0b-130">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="69d0b-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="69d0b-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="69d0b-132">Nome della modalità pipeline gestita</span><span class="sxs-lookup"><span data-stu-id="69d0b-132">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="69d0b-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="69d0b-133">-Name</span></span>
<span data-ttu-id="69d0b-134">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="69d0b-134">WebApp Name</span></span>

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

### <span data-ttu-id="69d0b-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="69d0b-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="69d0b-136">NET Framework</span><span class="sxs-lookup"><span data-stu-id="69d0b-136">Net Framework Version</span></span>

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

### <span data-ttu-id="69d0b-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="69d0b-137">-NumberOfWorkers</span></span>
<span data-ttu-id="69d0b-138">Numero di dipendenti da allocare</span><span class="sxs-lookup"><span data-stu-id="69d0b-138">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="69d0b-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="69d0b-139">-PhpVersion</span></span>
<span data-ttu-id="69d0b-140">Versione php</span><span class="sxs-lookup"><span data-stu-id="69d0b-140">Php Version</span></span>

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

### <span data-ttu-id="69d0b-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="69d0b-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="69d0b-142">Richiesta di traccia attivata</span><span class="sxs-lookup"><span data-stu-id="69d0b-142">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="69d0b-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69d0b-143">-ResourceGroupName</span></span>
<span data-ttu-id="69d0b-144">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="69d0b-144">Resource Group Name</span></span>

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

### <span data-ttu-id="69d0b-145">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="69d0b-145">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="69d0b-146">Usare il processo di lavoro a 32 bit Boolean</span><span class="sxs-lookup"><span data-stu-id="69d0b-146">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="69d0b-147">-Web App</span><span class="sxs-lookup"><span data-stu-id="69d0b-147">-WebApp</span></span>
<span data-ttu-id="69d0b-148">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="69d0b-148">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69d0b-149">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="69d0b-149">-WebSocketsEnabled</span></span>
<span data-ttu-id="69d0b-150">WebSocketsEnabled booleano</span><span class="sxs-lookup"><span data-stu-id="69d0b-150">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="69d0b-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69d0b-151">-DefaultProfile</span></span>
<span data-ttu-id="69d0b-152">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="69d0b-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69d0b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69d0b-153">CommonParameters</span></span>
<span data-ttu-id="69d0b-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69d0b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69d0b-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69d0b-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69d0b-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69d0b-156">INPUTS</span></span>

### <span data-ttu-id="69d0b-157">Int32</span><span class="sxs-lookup"><span data-stu-id="69d0b-157">Int32</span></span>
<span data-ttu-id="69d0b-158">Il parametro "NumberOfWorkers" accetta il valore di tipo "Int32" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="69d0b-158">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="69d0b-159">Sito</span><span class="sxs-lookup"><span data-stu-id="69d0b-159">Site</span></span>
<span data-ttu-id="69d0b-160">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="69d0b-160">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="69d0b-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69d0b-161">OUTPUTS</span></span>

## <span data-ttu-id="69d0b-162">Note</span><span class="sxs-lookup"><span data-stu-id="69d0b-162">NOTES</span></span>

## <span data-ttu-id="69d0b-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69d0b-163">RELATED LINKS</span></span>

[<span data-ttu-id="69d0b-164">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="69d0b-164">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="69d0b-165">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="69d0b-165">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="69d0b-166">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="69d0b-166">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="69d0b-167">Riavviare-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="69d0b-167">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="69d0b-168">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="69d0b-168">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="69d0b-169">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="69d0b-169">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
