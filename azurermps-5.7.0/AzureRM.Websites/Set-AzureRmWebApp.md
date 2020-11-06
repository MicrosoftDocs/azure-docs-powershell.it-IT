---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: 3587c7a725386976a04a9dc9922b3b0a16eb9362
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520313"
---
# <span data-ttu-id="25821-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="25821-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="25821-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="25821-102">SYNOPSIS</span></span>
<span data-ttu-id="25821-103">Modifica un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="25821-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25821-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="25821-104">SYNTAX</span></span>

### <span data-ttu-id="25821-105">S1</span><span class="sxs-lookup"><span data-stu-id="25821-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>]
 [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25821-106">S2</span><span class="sxs-lookup"><span data-stu-id="25821-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25821-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25821-107">DESCRIPTION</span></span>
<span data-ttu-id="25821-108">Il cmdlet **set-AzureRmWebApp** imposta una Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="25821-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="25821-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="25821-109">EXAMPLES</span></span>

### <span data-ttu-id="25821-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="25821-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="25821-111">Questo comando imposta HttpLoggingEnabled su true per l'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="25821-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="25821-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="25821-112">PARAMETERS</span></span>

### <span data-ttu-id="25821-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="25821-113">-AppServicePlan</span></span>
<span data-ttu-id="25821-114">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="25821-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="25821-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="25821-115">-AppSettings</span></span>
<span data-ttu-id="25821-116">HashTable delle impostazioni dell'app</span><span class="sxs-lookup"><span data-stu-id="25821-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="25821-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="25821-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="25821-118">Nome dello slot di destinazione per lo scambio automatico</span><span class="sxs-lookup"><span data-stu-id="25821-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="25821-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="25821-119">-ConnectionStrings</span></span>
<span data-ttu-id="25821-120">HashTable stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="25821-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="25821-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="25821-121">-DefaultDocuments</span></span>
<span data-ttu-id="25821-122">Matrice di stringhe documenti predefinita</span><span class="sxs-lookup"><span data-stu-id="25821-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="25821-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25821-123">-DefaultProfile</span></span>
<span data-ttu-id="25821-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="25821-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25821-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="25821-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="25821-126">Errore di registrazione dettagliata delle funzionalità booleane</span><span class="sxs-lookup"><span data-stu-id="25821-126">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="25821-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="25821-127">-HandlerMappings</span></span>
<span data-ttu-id="25821-128">Interfaccia di mapping dei gestori</span><span class="sxs-lookup"><span data-stu-id="25821-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="25821-129">-HostName</span><span class="sxs-lookup"><span data-stu-id="25821-129">-HostNames</span></span>
<span data-ttu-id="25821-130">Matrice di stringhe Web App HostNames</span><span class="sxs-lookup"><span data-stu-id="25821-130">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="25821-131">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="25821-131">-HttpLoggingEnabled</span></span>
<span data-ttu-id="25821-132">HttpLoggingEnabled booleano</span><span class="sxs-lookup"><span data-stu-id="25821-132">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="25821-133">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="25821-133">-ManagedPipelineMode</span></span>
<span data-ttu-id="25821-134">Nome della modalità pipeline gestita</span><span class="sxs-lookup"><span data-stu-id="25821-134">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="25821-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="25821-135">-Name</span></span>
<span data-ttu-id="25821-136">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="25821-136">WebApp Name</span></span>

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

### <span data-ttu-id="25821-137">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="25821-137">-NetFrameworkVersion</span></span>
<span data-ttu-id="25821-138">NET Framework</span><span class="sxs-lookup"><span data-stu-id="25821-138">Net Framework Version</span></span>

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

### <span data-ttu-id="25821-139">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="25821-139">-NumberOfWorkers</span></span>
<span data-ttu-id="25821-140">Numero di dipendenti da allocare</span><span class="sxs-lookup"><span data-stu-id="25821-140">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="25821-141">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="25821-141">-PhpVersion</span></span>
<span data-ttu-id="25821-142">Versione php</span><span class="sxs-lookup"><span data-stu-id="25821-142">Php Version</span></span>

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

### <span data-ttu-id="25821-143">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="25821-143">-RequestTracingEnabled</span></span>
<span data-ttu-id="25821-144">Richiesta di traccia attivata</span><span class="sxs-lookup"><span data-stu-id="25821-144">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="25821-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25821-145">-ResourceGroupName</span></span>
<span data-ttu-id="25821-146">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="25821-146">Resource Group Name</span></span>

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

### <span data-ttu-id="25821-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="25821-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="25821-148">Usare il processo di lavoro a 32 bit Boolean</span><span class="sxs-lookup"><span data-stu-id="25821-148">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="25821-149">-Web App</span><span class="sxs-lookup"><span data-stu-id="25821-149">-WebApp</span></span>
<span data-ttu-id="25821-150">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="25821-150">WebApp Object</span></span>

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

### <span data-ttu-id="25821-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="25821-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="25821-152">WebSocketsEnabled booleano</span><span class="sxs-lookup"><span data-stu-id="25821-152">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="25821-153">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25821-153">-AsJob</span></span>
<span data-ttu-id="25821-154">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="25821-154">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25821-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25821-155">CommonParameters</span></span>
<span data-ttu-id="25821-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25821-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25821-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25821-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25821-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="25821-158">INPUTS</span></span>

### <span data-ttu-id="25821-159">Int32</span><span class="sxs-lookup"><span data-stu-id="25821-159">Int32</span></span>
<span data-ttu-id="25821-160">Il parametro "NumberOfWorkers" accetta il valore di tipo "Int32" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="25821-160">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="25821-161">Sito</span><span class="sxs-lookup"><span data-stu-id="25821-161">Site</span></span>
<span data-ttu-id="25821-162">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="25821-162">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="25821-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="25821-163">OUTPUTS</span></span>

## <span data-ttu-id="25821-164">Note</span><span class="sxs-lookup"><span data-stu-id="25821-164">NOTES</span></span>

## <span data-ttu-id="25821-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="25821-165">RELATED LINKS</span></span>

[<span data-ttu-id="25821-166">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="25821-166">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="25821-167">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="25821-167">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="25821-168">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="25821-168">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="25821-169">Riavviare-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="25821-169">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="25821-170">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="25821-170">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="25821-171">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="25821-171">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
