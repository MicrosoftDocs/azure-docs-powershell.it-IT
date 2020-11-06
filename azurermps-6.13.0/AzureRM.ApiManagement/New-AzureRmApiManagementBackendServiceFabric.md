---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendServiceFabric.md
ms.openlocfilehash: 925e4949b444c9338fad3f88cf5066430e1b5a75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512039"
---
# <span data-ttu-id="b92c6-101">New-AzureRmApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b92c6-101">New-AzureRmApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="b92c6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b92c6-102">SYNOPSIS</span></span>
<span data-ttu-id="b92c6-103">Crea un oggetto di `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="b92c6-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b92c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b92c6-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendServiceFabric -ManagementEndpoint <String[]>
 -ClientCertificateThumbprint <String> [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>]
 [-ServerCertificateThumbprint <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b92c6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b92c6-105">DESCRIPTION</span></span>

<span data-ttu-id="b92c6-106">Il cmdlet **New-AzureRmApiManagementBackendServiceFabric** crea un oggetto `PsApiManagementServiceFabric` da usare in cmdlet **New-AzureRmApiManagementBackend** e **set-AzureRmApiManagementBackend**.</span><span class="sxs-lookup"><span data-stu-id="b92c6-106">The **New-AzureRmApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzureRmApiManagementBackend** and **Set-AzureRmApiManagementBackend**.</span></span>

## <span data-ttu-id="b92c6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b92c6-107">EXAMPLES</span></span>

### <span data-ttu-id="b92c6-108">Esempio 1: creare un oggetto In-Memory tessuto del servizio back-end</span><span class="sxs-lookup"><span data-stu-id="b92c6-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzureRmApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="b92c6-109">Crea un contratto del tessuto del servizio back-end</span><span class="sxs-lookup"><span data-stu-id="b92c6-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="b92c6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b92c6-110">PARAMETERS</span></span>

### <span data-ttu-id="b92c6-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="b92c6-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="b92c6-112">Identificazione personale del certificato client per l'endpoint di gestione.</span><span class="sxs-lookup"><span data-stu-id="b92c6-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="b92c6-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b92c6-113">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b92c6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b92c6-114">-DefaultProfile</span></span>
<span data-ttu-id="b92c6-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b92c6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b92c6-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="b92c6-116">-ManagementEndpoint</span></span>
<span data-ttu-id="b92c6-117">Endpoint di gestione dei cluster di servizi in tessuto.</span><span class="sxs-lookup"><span data-stu-id="b92c6-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="b92c6-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b92c6-118">This parameter is required.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b92c6-119">-MaxPartitionResolutionRetry</span><span class="sxs-lookup"><span data-stu-id="b92c6-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="b92c6-120">Numero massimo di tentativi per la risoluzione di una partizione del tessuto del servizio.</span><span class="sxs-lookup"><span data-stu-id="b92c6-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="b92c6-121">Questo parametro è facoltativo e il valore predefinito è 5.</span><span class="sxs-lookup"><span data-stu-id="b92c6-121">This parameter is optional and default value is 5.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b92c6-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="b92c6-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="b92c6-123">Identificazione personale del servizio di gestione cluster certificati utilizza per la comunicazione TLS. Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b92c6-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b92c6-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="b92c6-124">-ServerX509Name</span></span>
<span data-ttu-id="b92c6-125">Raccolta nomi certificati X509 server.</span><span class="sxs-lookup"><span data-stu-id="b92c6-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="b92c6-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b92c6-126">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b92c6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b92c6-127">CommonParameters</span></span>
<span data-ttu-id="b92c6-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b92c6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b92c6-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b92c6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b92c6-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b92c6-130">INPUTS</span></span>

### <span data-ttu-id="b92c6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b92c6-131">System.String</span></span>

## <span data-ttu-id="b92c6-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b92c6-132">OUTPUTS</span></span>

### <span data-ttu-id="b92c6-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b92c6-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="b92c6-134">Note</span><span class="sxs-lookup"><span data-stu-id="b92c6-134">NOTES</span></span>

## <span data-ttu-id="b92c6-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b92c6-135">RELATED LINKS</span></span>

[<span data-ttu-id="b92c6-136">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b92c6-136">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="b92c6-137">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b92c6-137">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="b92c6-138">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="b92c6-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="b92c6-139">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b92c6-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="b92c6-140">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b92c6-140">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
