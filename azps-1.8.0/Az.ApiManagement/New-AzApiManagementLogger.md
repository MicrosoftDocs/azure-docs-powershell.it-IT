---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementLogger.md
ms.openlocfilehash: 3df5f6974cd955035c16972a5a7358aa44a30390
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685132"
---
# <span data-ttu-id="f4ebf-101">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="f4ebf-101">New-AzApiManagementLogger</span></span>

## <span data-ttu-id="f4ebf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4ebf-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ebf-103">Crea un logger di gestione API.</span><span class="sxs-lookup"><span data-stu-id="f4ebf-103">Creates an API Management Logger.</span></span>

## <span data-ttu-id="f4ebf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4ebf-104">SYNTAX</span></span>

### <span data-ttu-id="f4ebf-105">EventHubLoggerSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f4ebf-105">EventHubLoggerSet (Default)</span></span>
```
New-AzApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4ebf-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="f4ebf-106">ApplicationInsightsLoggerSet</span></span>
```
New-AzApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -InstrumentationKey <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4ebf-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4ebf-107">DESCRIPTION</span></span>
<span data-ttu-id="f4ebf-108">Il cmdlet **New-AzApiManagementLogger** crea un **logger** di gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ebf-108">The **New-AzApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="f4ebf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4ebf-109">EXAMPLES</span></span>

### <span data-ttu-id="f4ebf-110">Esempio 1: creare un logger</span><span class="sxs-lookup"><span data-stu-id="f4ebf-110">Example 1: Create a logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="f4ebf-111">Questo comando crea un logger denominato ContosoSdkEventHub usando la stringa di connessione specificata.</span><span class="sxs-lookup"><span data-stu-id="f4ebf-111">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="f4ebf-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4ebf-112">PARAMETERS</span></span>

### <span data-ttu-id="f4ebf-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="f4ebf-113">-ConnectionString</span></span>
<span data-ttu-id="f4ebf-114">Specifica una stringa di connessione hub eventi di Azure che inizia con le operazioni seguenti: `Endpoint=endpoint and key from Azure classic portal`</span><span class="sxs-lookup"><span data-stu-id="f4ebf-114">Specifies an Azure Event Hubs connection string that starts with the following: `Endpoint=endpoint and key from Azure classic portal`</span></span>
<span data-ttu-id="f4ebf-115">La chiave con i diritti di invio nella stringa di connessione deve essere configurata.</span><span class="sxs-lookup"><span data-stu-id="f4ebf-115">The Key with Send Rights in the connection string must be configured.</span></span>

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

### <span data-ttu-id="f4ebf-116">-Contesto</span><span class="sxs-lookup"><span data-stu-id="f4ebf-116">-Context</span></span>
<span data-ttu-id="f4ebf-117">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f4ebf-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f4ebf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ebf-118">-DefaultProfile</span></span>
<span data-ttu-id="f4ebf-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ebf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4ebf-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4ebf-120">-Description</span></span>
<span data-ttu-id="f4ebf-121">Specifica una descrizione.</span><span class="sxs-lookup"><span data-stu-id="f4ebf-121">Specifies a description.</span></span>

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

### <span data-ttu-id="f4ebf-122">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="f4ebf-122">-InstrumentationKey</span></span>
<span data-ttu-id="f4ebf-123">Chiave di strumentazione degli approfondimenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f4ebf-123">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="f4ebf-124">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f4ebf-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="f4ebf-125">-Buffered</span><span class="sxs-lookup"><span data-stu-id="f4ebf-125">-IsBuffered</span></span>
<span data-ttu-id="f4ebf-126">Specifica se i record nel logger vengono memorizzati nel buffer prima della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="f4ebf-126">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="f4ebf-127">Il valore predefinito è $True.</span><span class="sxs-lookup"><span data-stu-id="f4ebf-127">The default value is $True.</span></span>
<span data-ttu-id="f4ebf-128">Quando i record vengono memorizzati nel buffer, vengono inviati agli hub eventi ogni 15 secondi o ogni volta che il buffer riceve 256 KB di messaggi.</span><span class="sxs-lookup"><span data-stu-id="f4ebf-128">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="f4ebf-129">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="f4ebf-129">-LoggerId</span></span>
<span data-ttu-id="f4ebf-130">Specifica un ID per il logger.</span><span class="sxs-lookup"><span data-stu-id="f4ebf-130">Specifies an ID for the logger.</span></span>
<span data-ttu-id="f4ebf-131">Se non specifichi un ID, questo cmdlet ne genera uno.</span><span class="sxs-lookup"><span data-stu-id="f4ebf-131">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="f4ebf-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4ebf-132">-Name</span></span>
<span data-ttu-id="f4ebf-133">Specifica il nome dell'entità di un hub eventi di Azure Classic Portal.</span><span class="sxs-lookup"><span data-stu-id="f4ebf-133">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="f4ebf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ebf-134">CommonParameters</span></span>
<span data-ttu-id="f4ebf-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4ebf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ebf-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4ebf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ebf-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4ebf-137">INPUTS</span></span>

### <span data-ttu-id="f4ebf-138">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f4ebf-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f4ebf-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f4ebf-139">System.String</span></span>

### <span data-ttu-id="f4ebf-140">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f4ebf-140">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f4ebf-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4ebf-141">OUTPUTS</span></span>

### <span data-ttu-id="f4ebf-142">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="f4ebf-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="f4ebf-143">Note</span><span class="sxs-lookup"><span data-stu-id="f4ebf-143">NOTES</span></span>

## <span data-ttu-id="f4ebf-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4ebf-144">RELATED LINKS</span></span>

[<span data-ttu-id="f4ebf-145">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="f4ebf-145">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="f4ebf-146">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="f4ebf-146">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="f4ebf-147">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="f4ebf-147">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)

