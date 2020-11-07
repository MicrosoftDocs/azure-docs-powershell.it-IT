---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
ms.openlocfilehash: 04119d70f1cf3ae01b1d74e24cb2e030eecaa46b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685457"
---
# <span data-ttu-id="e367d-101">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e367d-101">New-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="e367d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e367d-102">SYNOPSIS</span></span>
<span data-ttu-id="e367d-103">Crea un logger di gestione API.</span><span class="sxs-lookup"><span data-stu-id="e367d-103">Creates an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e367d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e367d-104">SYNTAX</span></span>

### <span data-ttu-id="e367d-105">EventHubLoggerSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e367d-105">EventHubLoggerSet (Default)</span></span>
```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e367d-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="e367d-106">ApplicationInsightsLoggerSet</span></span>
```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>]
 -InstrumentationKey <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e367d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e367d-107">DESCRIPTION</span></span>
<span data-ttu-id="e367d-108">Il cmdlet **New-AzureRmApiManagementLogger** crea un **logger** di gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="e367d-108">The **New-AzureRmApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="e367d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e367d-109">EXAMPLES</span></span>

### <span data-ttu-id="e367d-110">Esempio 1: creare un logger</span><span class="sxs-lookup"><span data-stu-id="e367d-110">Example 1: Create a logger</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="e367d-111">Questo comando crea un logger denominato ContosoSdkEventHub usando la stringa di connessione specificata.</span><span class="sxs-lookup"><span data-stu-id="e367d-111">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="e367d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e367d-112">PARAMETERS</span></span>

### <span data-ttu-id="e367d-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="e367d-113">-ConnectionString</span></span>
<span data-ttu-id="e367d-114">Specifica una stringa di connessione hub eventi di Azure che inizia con le operazioni seguenti: `Endpoint=endpoint and key from Azure classic portal`</span><span class="sxs-lookup"><span data-stu-id="e367d-114">Specifies an Azure Event Hubs connection string that starts with the following: `Endpoint=endpoint and key from Azure classic portal`</span></span>
<span data-ttu-id="e367d-115">La chiave con i diritti di invio nella stringa di connessione deve essere configurata.</span><span class="sxs-lookup"><span data-stu-id="e367d-115">The Key with Send Rights in the connection string must be configured.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e367d-116">-Contesto</span><span class="sxs-lookup"><span data-stu-id="e367d-116">-Context</span></span>
<span data-ttu-id="e367d-117">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="e367d-117">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e367d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e367d-118">-DefaultProfile</span></span>
<span data-ttu-id="e367d-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e367d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e367d-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="e367d-120">-Description</span></span>
<span data-ttu-id="e367d-121">Specifica una descrizione.</span><span class="sxs-lookup"><span data-stu-id="e367d-121">Specifies a description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e367d-122">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="e367d-122">-InstrumentationKey</span></span>
<span data-ttu-id="e367d-123">Chiave di strumentazione degli approfondimenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e367d-123">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="e367d-124">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e367d-124">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationInsightsLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e367d-125">-Buffered</span><span class="sxs-lookup"><span data-stu-id="e367d-125">-IsBuffered</span></span>
<span data-ttu-id="e367d-126">Specifica se i record nel logger vengono memorizzati nel buffer prima della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="e367d-126">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="e367d-127">Il valore predefinito è $True.</span><span class="sxs-lookup"><span data-stu-id="e367d-127">The default value is $True.</span></span>
<span data-ttu-id="e367d-128">Quando i record vengono memorizzati nel buffer, vengono inviati agli hub eventi ogni 15 secondi o ogni volta che il buffer riceve 256 KB di messaggi.</span><span class="sxs-lookup"><span data-stu-id="e367d-128">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e367d-129">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="e367d-129">-LoggerId</span></span>
<span data-ttu-id="e367d-130">Specifica un ID per il logger.</span><span class="sxs-lookup"><span data-stu-id="e367d-130">Specifies an ID for the logger.</span></span>
<span data-ttu-id="e367d-131">Se non specifichi un ID, questo cmdlet ne genera uno.</span><span class="sxs-lookup"><span data-stu-id="e367d-131">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e367d-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="e367d-132">-Name</span></span>
<span data-ttu-id="e367d-133">Specifica il nome dell'entità di un hub eventi di Azure Classic Portal.</span><span class="sxs-lookup"><span data-stu-id="e367d-133">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e367d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e367d-134">CommonParameters</span></span>
<span data-ttu-id="e367d-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e367d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e367d-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e367d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e367d-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e367d-137">INPUTS</span></span>

### <span data-ttu-id="e367d-138">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e367d-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e367d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e367d-139">System.String</span></span>

### <span data-ttu-id="e367d-140">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e367d-140">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e367d-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e367d-141">OUTPUTS</span></span>

### <span data-ttu-id="e367d-142">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e367d-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="e367d-143">Note</span><span class="sxs-lookup"><span data-stu-id="e367d-143">NOTES</span></span>

## <span data-ttu-id="e367d-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e367d-144">RELATED LINKS</span></span>

[<span data-ttu-id="e367d-145">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e367d-145">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="e367d-146">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e367d-146">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="e367d-147">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e367d-147">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


