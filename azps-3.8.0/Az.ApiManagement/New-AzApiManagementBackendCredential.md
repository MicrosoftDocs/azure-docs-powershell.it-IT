---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: c1495c505653470f4aa6b818162d57e02893c5e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020217"
---
# <span data-ttu-id="2b7fb-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="2b7fb-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="2b7fb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b7fb-102">SYNOPSIS</span></span>
<span data-ttu-id="2b7fb-103">Crea un nuovo contratto di credenziale back-end.</span><span class="sxs-lookup"><span data-stu-id="2b7fb-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="2b7fb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b7fb-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b7fb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b7fb-105">DESCRIPTION</span></span>
<span data-ttu-id="2b7fb-106">Crea un nuovo contratto di credenziale back-end.</span><span class="sxs-lookup"><span data-stu-id="2b7fb-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="2b7fb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b7fb-107">EXAMPLES</span></span>

### <span data-ttu-id="2b7fb-108">Creare un oggetto In-Memory credenziali di backend</span><span class="sxs-lookup"><span data-stu-id="2b7fb-108">Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="2b7fb-109">Crea un contratto di credenziali back-end</span><span class="sxs-lookup"><span data-stu-id="2b7fb-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="2b7fb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b7fb-110">PARAMETERS</span></span>

### <span data-ttu-id="2b7fb-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="2b7fb-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="2b7fb-112">Intestazione di autorizzazione usata per il backend.</span><span class="sxs-lookup"><span data-stu-id="2b7fb-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="2b7fb-113">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2b7fb-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b7fb-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="2b7fb-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="2b7fb-115">Schema di autorizzazione usato per il backend.</span><span class="sxs-lookup"><span data-stu-id="2b7fb-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="2b7fb-116">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2b7fb-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b7fb-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="2b7fb-117">-CertificateThumbprint</span></span>
<span data-ttu-id="2b7fb-118">Identificazioni personali del certificato client.</span><span class="sxs-lookup"><span data-stu-id="2b7fb-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="2b7fb-119">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2b7fb-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="2b7fb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b7fb-120">-DefaultProfile</span></span>
<span data-ttu-id="2b7fb-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b7fb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b7fb-122">-Intestazione</span><span class="sxs-lookup"><span data-stu-id="2b7fb-122">-Header</span></span>
<span data-ttu-id="2b7fb-123">Valori dei parametri di intestazione accettati da backend.</span><span class="sxs-lookup"><span data-stu-id="2b7fb-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="2b7fb-124">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2b7fb-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="2b7fb-125">-Query</span><span class="sxs-lookup"><span data-stu-id="2b7fb-125">-Query</span></span>
<span data-ttu-id="2b7fb-126">Valori dei parametri di query accettati da backend.</span><span class="sxs-lookup"><span data-stu-id="2b7fb-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="2b7fb-127">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2b7fb-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="2b7fb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b7fb-128">CommonParameters</span></span>
<span data-ttu-id="2b7fb-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b7fb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b7fb-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b7fb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b7fb-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b7fb-131">INPUTS</span></span>

### <span data-ttu-id="2b7fb-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2b7fb-132">None</span></span>

## <span data-ttu-id="2b7fb-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b7fb-133">OUTPUTS</span></span>

### <span data-ttu-id="2b7fb-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="2b7fb-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="2b7fb-135">Note</span><span class="sxs-lookup"><span data-stu-id="2b7fb-135">NOTES</span></span>

## <span data-ttu-id="2b7fb-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b7fb-136">RELATED LINKS</span></span>

[<span data-ttu-id="2b7fb-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2b7fb-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="2b7fb-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2b7fb-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="2b7fb-139">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="2b7fb-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="2b7fb-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2b7fb-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="2b7fb-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2b7fb-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
