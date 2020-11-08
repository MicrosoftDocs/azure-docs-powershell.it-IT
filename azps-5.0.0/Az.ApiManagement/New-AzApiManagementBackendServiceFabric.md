---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
ms.openlocfilehash: 352e40aa64adf5eea98950ac9271f0237e634ab6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202592"
---
# <span data-ttu-id="792f9-101">New-AzApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="792f9-101">New-AzApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="792f9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="792f9-102">SYNOPSIS</span></span>
<span data-ttu-id="792f9-103">Crea un oggetto di `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="792f9-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

## <span data-ttu-id="792f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="792f9-104">SYNTAX</span></span>

```
New-AzApiManagementBackendServiceFabric -ManagementEndpoint <String[]> -ClientCertificateThumbprint <String>
 [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>] [-ServerCertificateThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="792f9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="792f9-105">DESCRIPTION</span></span>

<span data-ttu-id="792f9-106">Il cmdlet **New-AzApiManagementBackendServiceFabric** crea un oggetto `PsApiManagementServiceFabric` da usare in cmdlet **New-AzApiManagementBackend** e **set-AzApiManagementBackend**.</span><span class="sxs-lookup"><span data-stu-id="792f9-106">The **New-AzApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzApiManagementBackend** and **Set-AzApiManagementBackend**.</span></span>

## <span data-ttu-id="792f9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="792f9-107">EXAMPLES</span></span>

### <span data-ttu-id="792f9-108">Esempio 1: creare un oggetto In-Memory tessuto del servizio back-end</span><span class="sxs-lookup"><span data-stu-id="792f9-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="792f9-109">Crea un contratto del tessuto del servizio back-end</span><span class="sxs-lookup"><span data-stu-id="792f9-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="792f9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="792f9-110">PARAMETERS</span></span>

### <span data-ttu-id="792f9-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="792f9-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="792f9-112">Identificazione personale del certificato client per l'endpoint di gestione.</span><span class="sxs-lookup"><span data-stu-id="792f9-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="792f9-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="792f9-113">This parameter is required.</span></span>

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

### <span data-ttu-id="792f9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="792f9-114">-DefaultProfile</span></span>
<span data-ttu-id="792f9-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="792f9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="792f9-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="792f9-116">-ManagementEndpoint</span></span>
<span data-ttu-id="792f9-117">Endpoint di gestione dei cluster di servizi in tessuto.</span><span class="sxs-lookup"><span data-stu-id="792f9-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="792f9-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="792f9-118">This parameter is required.</span></span>

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

### <span data-ttu-id="792f9-119">-MaxPartitionResolutionRetry</span><span class="sxs-lookup"><span data-stu-id="792f9-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="792f9-120">Numero massimo di tentativi per la risoluzione di una partizione del tessuto del servizio.</span><span class="sxs-lookup"><span data-stu-id="792f9-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="792f9-121">Questo parametro è facoltativo e il valore predefinito è 5.</span><span class="sxs-lookup"><span data-stu-id="792f9-121">This parameter is optional and default value is 5.</span></span>

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

### <span data-ttu-id="792f9-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="792f9-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="792f9-123">Identificazione personale del servizio di gestione cluster certificati utilizza per la comunicazione TLS. Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="792f9-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

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

### <span data-ttu-id="792f9-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="792f9-124">-ServerX509Name</span></span>
<span data-ttu-id="792f9-125">Raccolta nomi certificati X509 server.</span><span class="sxs-lookup"><span data-stu-id="792f9-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="792f9-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="792f9-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="792f9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="792f9-127">CommonParameters</span></span>
<span data-ttu-id="792f9-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="792f9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="792f9-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="792f9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="792f9-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="792f9-130">INPUTS</span></span>

### <span data-ttu-id="792f9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="792f9-131">System.String</span></span>

## <span data-ttu-id="792f9-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="792f9-132">OUTPUTS</span></span>

### <span data-ttu-id="792f9-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="792f9-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="792f9-134">Note</span><span class="sxs-lookup"><span data-stu-id="792f9-134">NOTES</span></span>

## <span data-ttu-id="792f9-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="792f9-135">RELATED LINKS</span></span>

[<span data-ttu-id="792f9-136">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="792f9-136">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="792f9-137">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="792f9-137">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="792f9-138">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="792f9-138">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="792f9-139">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="792f9-139">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="792f9-140">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="792f9-140">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
