---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
ms.openlocfilehash: 352e40aa64adf5eea98950ac9271f0237e634ab6
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398139"
---
# <span data-ttu-id="4e560-101">New-AzApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4e560-101">New-AzApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="4e560-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e560-102">SYNOPSIS</span></span>
<span data-ttu-id="4e560-103">Crea un oggetto di `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="4e560-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

## <span data-ttu-id="4e560-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e560-104">SYNTAX</span></span>

```
New-AzApiManagementBackendServiceFabric -ManagementEndpoint <String[]> -ClientCertificateThumbprint <String>
 [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>] [-ServerCertificateThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e560-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4e560-105">DESCRIPTION</span></span>

<span data-ttu-id="4e560-106">Il cmdlet **New-AzApiManagementBackendServiceFabric** crea un oggetto di cui usare i `PsApiManagementServiceFabric` cmdlet **New-AzApiManagementBackend** e **Set-AzApiManagementBackend.**</span><span class="sxs-lookup"><span data-stu-id="4e560-106">The **New-AzApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzApiManagementBackend** and **Set-AzApiManagementBackend**.</span></span>

## <span data-ttu-id="4e560-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e560-107">EXAMPLES</span></span>

### <span data-ttu-id="4e560-108">Esempio 1: Creare un oggetto In-Memory Backend Service Fabric</span><span class="sxs-lookup"><span data-stu-id="4e560-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="4e560-109">Crea un contratto Back-Service Fabric</span><span class="sxs-lookup"><span data-stu-id="4e560-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="4e560-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e560-110">PARAMETERS</span></span>

### <span data-ttu-id="4e560-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="4e560-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="4e560-112">Thumbprint certificato client per l'endpoint di gestione.</span><span class="sxs-lookup"><span data-stu-id="4e560-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="4e560-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="4e560-113">This parameter is required.</span></span>

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

### <span data-ttu-id="4e560-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e560-114">-DefaultProfile</span></span>
<span data-ttu-id="4e560-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e560-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e560-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="4e560-116">-ManagementEndpoint</span></span>
<span data-ttu-id="4e560-117">Endpoint di gestione del cluster Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="4e560-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="4e560-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="4e560-118">This parameter is required.</span></span>

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

### <span data-ttu-id="4e560-119">-MaxPartitionResolutionRetry</span><span class="sxs-lookup"><span data-stu-id="4e560-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="4e560-120">Numero massimo di tentativi durante la risoluzione di una partizione Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="4e560-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="4e560-121">Questo parametro è facoltativo e il valore predefinito è 5.</span><span class="sxs-lookup"><span data-stu-id="4e560-121">This parameter is optional and default value is 5.</span></span>

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

### <span data-ttu-id="4e560-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="4e560-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="4e560-123">Thumbprint dei certificati utilizzati dal servizio di gestione cluster per la comunicazione TLS. Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="4e560-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

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

### <span data-ttu-id="4e560-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="4e560-124">-ServerX509Name</span></span>
<span data-ttu-id="4e560-125">Raccolta di nomi di certificati del server X509.</span><span class="sxs-lookup"><span data-stu-id="4e560-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="4e560-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="4e560-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="4e560-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e560-127">CommonParameters</span></span>
<span data-ttu-id="4e560-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e560-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e560-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4e560-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e560-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="4e560-130">INPUTS</span></span>

### <span data-ttu-id="4e560-131">System.String</span><span class="sxs-lookup"><span data-stu-id="4e560-131">System.String</span></span>

## <span data-ttu-id="4e560-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e560-132">OUTPUTS</span></span>

### <span data-ttu-id="4e560-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4e560-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="4e560-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="4e560-134">NOTES</span></span>

## <span data-ttu-id="4e560-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e560-135">RELATED LINKS</span></span>

[<span data-ttu-id="4e560-136">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="4e560-136">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="4e560-137">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="4e560-137">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="4e560-138">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="4e560-138">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="4e560-139">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="4e560-139">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="4e560-140">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="4e560-140">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
