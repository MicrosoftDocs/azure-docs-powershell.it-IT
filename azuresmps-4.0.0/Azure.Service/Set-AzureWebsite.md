---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9D821623-DEF9-49E4-9C44-10643A92A2E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f6690aa45125a0d1b3383b08443234f47a1f7e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023391"
---
# <span data-ttu-id="ee1d8-101">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ee1d8-101">Set-AzureWebsite</span></span>

## <span data-ttu-id="ee1d8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee1d8-102">SYNOPSIS</span></span>
<span data-ttu-id="ee1d8-103">Configura un sito Web in uso in Azure.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-103">Configures a website running in Azure.</span></span>

## <span data-ttu-id="ee1d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee1d8-104">SYNTAX</span></span>

```
Set-AzureWebsite [-NumberOfWorkers <Int32>] [-DefaultDocuments <String[]>] [-NetFrameworkVersion <String>]
 [-PhpVersion <String>] [-RequestTracingEnabled <Boolean>] [-HttpLoggingEnabled <Boolean>]
 [-DetailedErrorLoggingEnabled <Boolean>] [-HostNames <String[]>] [-AppSettings <Hashtable>]
 [-Metadata <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.NameValuePair]>]
 [-ConnectionStrings <ConnStringPropertyBag>] [-HandlerMappings <HandlerMapping[]>]
 [-SiteWithConfig <SiteWithConfig>] [-PassThru] [-ManagedPipelineMode <ManagedPipelineMode>]
 [-WebSocketsEnabled <Boolean>]
 [-RoutingRules <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.RoutingRule]>]
 [-Use32BitWorkerProcess <Boolean>] [-AutoSwapSlotName <String>]
 [-SlotStickyAppSettingNames <System.Collections.Generic.List`1[System.String]>]
 [-SlotStickyConnectionStringNames <System.Collections.Generic.List`1[System.String]>] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ee1d8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee1d8-105">DESCRIPTION</span></span>
<span data-ttu-id="ee1d8-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ee1d8-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ee1d8-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ee1d8-108">Il cmdlet **set-AzureWebsite** configura un sito Web in uso in Azure.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-108">The **Set-AzureWebsite** cmdlet configures a website running in Azure.</span></span>

## <span data-ttu-id="ee1d8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee1d8-109">EXAMPLES</span></span>

### <span data-ttu-id="ee1d8-110">Esempio 1: abilitare la registrazione HTTP per un sito Web</span><span class="sxs-lookup"><span data-stu-id="ee1d8-110">Example 1: Enable HTTP logging for a website</span></span>
```
PS C:\> Set-AzureWebsite -HttpLoggingEnabled 1
```

<span data-ttu-id="ee1d8-111">Questo esempio Abilita la registrazione HTTP.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-111">This example enables HTTP logging.</span></span>

### <span data-ttu-id="ee1d8-112">Esempio 2: impostare le credenziali di archiviazione per un sito Web</span><span class="sxs-lookup"><span data-stu-id="ee1d8-112">Example 2: Set storage credentials for a website</span></span>
```
PS C:\> $settings = New-Object Hashtable$settings["AZURE_STORAGE_ACCOUNT"= myaccountname$settings["AZURE_STORAGE_ACCESS_KEY"] = myaccesskeySet-AzureWebsite -AppSettings $settings myWebsite
```

<span data-ttu-id="ee1d8-113">Questo esempio imposta le credenziali di archiviazione in un sito Web denominato sito Web con variabili di ambiente per AZURE_STORAGE_ACCOUNT e AZURE_STORAGE_ACCESS_KEY.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-113">This example sets storage credentials in a website named myWebsite with environment variables for AZURE_STORAGE_ACCOUNT and AZURE_STORAGE_ACCESS_KEY.</span></span>

## <span data-ttu-id="ee1d8-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee1d8-114">PARAMETERS</span></span>

### <span data-ttu-id="ee1d8-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="ee1d8-115">-AppSettings</span></span>
<span data-ttu-id="ee1d8-116">Specifica le variabili di ambiente che verranno usate dal sito Web.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-116">Specifies the environment variables that will be used by the website.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1d8-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="ee1d8-117">-AutoSwapSlotName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1d8-118">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="ee1d8-118">-ConnectionStrings</span></span>
<span data-ttu-id="ee1d8-119">Specifica le stringhe di connessione usate dal sito Web.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-119">Specifies the connection strings used by the website.</span></span>

```yaml
Type: ConnStringPropertyBag
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1d8-120">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="ee1d8-120">-DefaultDocuments</span></span>
<span data-ttu-id="ee1d8-121">Specifica i documenti che vengono visualizzati automaticamente durante l'esplorazione del sito Web.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-121">Specifies the documents that are automatically displayed when browsing the website.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1d8-122">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="ee1d8-122">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="ee1d8-123">Determina se sono stati registrati errori di IIS dettagliati per il sito Web.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-123">Determines whether detailed IIS errors are logged for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1d8-124">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="ee1d8-124">-HandlerMappings</span></span>
<span data-ttu-id="ee1d8-125">Specifica i mapping dei gestori usati dal sito Web.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-125">Specifies the handler mappings used by the website.</span></span>

```yaml
Type: HandlerMapping[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1d8-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="ee1d8-126">-HostNames</span></span>
<span data-ttu-id="ee1d8-127">Specifica i nomi host completi che possono essere usati per accedere al sito Web.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-127">Specifies the fully qualified host names that can be used to access the website.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1d8-128">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="ee1d8-128">-HttpLoggingEnabled</span></span>
<span data-ttu-id="ee1d8-129">Determina se la registrazione http è abilitata per il sito Web.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-129">Determines whether http logging is enabled for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1d8-130">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="ee1d8-130">-ManagedPipelineMode</span></span>
<span data-ttu-id="ee1d8-131">Specifica la modalità pipeline gestita.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-131">Specifies the managed pipeline mode.</span></span>

```yaml
Type: ManagedPipelineMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1d8-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="ee1d8-132">-Metadata</span></span>
<span data-ttu-id="ee1d8-133">Specifica i metadati per il sito Web.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-133">Specifies the metadata for the website.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.NameValuePair]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1d8-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee1d8-134">-Name</span></span>
<span data-ttu-id="ee1d8-135">Specifica il nome del sito Web.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-135">Specifies the name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1d8-136">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="ee1d8-136">-NetFrameworkVersion</span></span>
<span data-ttu-id="ee1d8-137">Specifica la versione di .NET Framework necessaria per il sito Web.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-137">Specifies the version of the .Net Framework required by the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1d8-138">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="ee1d8-138">-NumberOfWorkers</span></span>
<span data-ttu-id="ee1d8-139">Specifica il numero di processi di lavoro in cui è in corso il sito Web.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-139">Specifies the number of worker processes running the website.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1d8-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee1d8-140">-PassThru</span></span>
<span data-ttu-id="ee1d8-141">Indica che questo cmdlet restituisce un valore **booleano** .</span><span class="sxs-lookup"><span data-stu-id="ee1d8-141">Indicates that this cmdlet returns a **Boolean** value.</span></span>

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

### <span data-ttu-id="ee1d8-142">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="ee1d8-142">-PhpVersion</span></span>
<span data-ttu-id="ee1d8-143">Specifica la versione PHP richiesta dal sito Web.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-143">Specifies the PHP version required by the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1d8-144">-Profile</span><span class="sxs-lookup"><span data-stu-id="ee1d8-144">-Profile</span></span>
<span data-ttu-id="ee1d8-145">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ee1d8-146">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee1d8-147">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="ee1d8-147">-RequestTracingEnabled</span></span>
<span data-ttu-id="ee1d8-148">Determina se la traccia delle richieste è abilitata per il sito Web.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-148">Determines whether request tracing is enabled for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1d8-149">-RoutingRules</span><span class="sxs-lookup"><span data-stu-id="ee1d8-149">-RoutingRules</span></span>
<span data-ttu-id="ee1d8-150">Specifica le regole di routing da usare per i test in produzione.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-150">Specifies the routing rules to use for testing in production.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.RoutingRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1d8-151">-SiteWithConfig</span><span class="sxs-lookup"><span data-stu-id="ee1d8-151">-SiteWithConfig</span></span>
<span data-ttu-id="ee1d8-152">Specifica la configurazione usata dal sito Web.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-152">Specifies the configuration used by the website.</span></span>

```yaml
Type: SiteWithConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1d8-153">-Slot</span><span class="sxs-lookup"><span data-stu-id="ee1d8-153">-Slot</span></span>
<span data-ttu-id="ee1d8-154">Specifica il nome dello slot del sito Web.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-154">Specifies the slot name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1d8-155">-SlotStickyAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="ee1d8-155">-SlotStickyAppSettingNames</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1d8-156">-SlotStickyConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="ee1d8-156">-SlotStickyConnectionStringNames</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1d8-157">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="ee1d8-157">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="ee1d8-158">Specifica se abilitare la modalità a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-158">Specifies whether to enable 32-bit mode.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1d8-159">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="ee1d8-159">-WebSocketsEnabled</span></span>
<span data-ttu-id="ee1d8-160">Specifica se abilitare WebSockets.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-160">Specifies whether to enable WebSockets.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1d8-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee1d8-161">CommonParameters</span></span>
<span data-ttu-id="ee1d8-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee1d8-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee1d8-163">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee1d8-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee1d8-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee1d8-164">INPUTS</span></span>

## <span data-ttu-id="ee1d8-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee1d8-165">OUTPUTS</span></span>

## <span data-ttu-id="ee1d8-166">Note</span><span class="sxs-lookup"><span data-stu-id="ee1d8-166">NOTES</span></span>

## <span data-ttu-id="ee1d8-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee1d8-167">RELATED LINKS</span></span>

[<span data-ttu-id="ee1d8-168">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ee1d8-168">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="ee1d8-169">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ee1d8-169">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="ee1d8-170">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ee1d8-170">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)


