---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
ms.openlocfilehash: d34a7666e10fe678d49194887d9b58e7c1ba0aa7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512043"
---
# <span data-ttu-id="bc109-101">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="bc109-101">New-AzureRmApiManagementBackendCredential</span></span>

## <span data-ttu-id="bc109-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bc109-102">SYNOPSIS</span></span>
<span data-ttu-id="bc109-103">Crea un nuovo contratto di credenziale back-end.</span><span class="sxs-lookup"><span data-stu-id="bc109-103">Creates a new Backend Credential contract.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc109-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc109-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc109-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc109-105">DESCRIPTION</span></span>
<span data-ttu-id="bc109-106">Crea un nuovo contratto di credenziale back-end.</span><span class="sxs-lookup"><span data-stu-id="bc109-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="bc109-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc109-107">EXAMPLES</span></span>

### <span data-ttu-id="bc109-108">Creare un oggetto In-Memory credenziali di backend</span><span class="sxs-lookup"><span data-stu-id="bc109-108">Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="bc109-109">Crea un contratto di credenziali back-end</span><span class="sxs-lookup"><span data-stu-id="bc109-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="bc109-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bc109-110">PARAMETERS</span></span>

### <span data-ttu-id="bc109-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="bc109-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="bc109-112">Intestazione di autorizzazione usata per il backend.</span><span class="sxs-lookup"><span data-stu-id="bc109-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="bc109-113">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bc109-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="bc109-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="bc109-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="bc109-115">Schema di autorizzazione usato per il backend.</span><span class="sxs-lookup"><span data-stu-id="bc109-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="bc109-116">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bc109-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="bc109-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="bc109-117">-CertificateThumbprint</span></span>
<span data-ttu-id="bc109-118">Identificazioni personali del certificato client.</span><span class="sxs-lookup"><span data-stu-id="bc109-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="bc109-119">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bc109-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="bc109-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc109-120">-DefaultProfile</span></span>
<span data-ttu-id="bc109-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc109-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc109-122">-Intestazione</span><span class="sxs-lookup"><span data-stu-id="bc109-122">-Header</span></span>
<span data-ttu-id="bc109-123">Valori dei parametri di intestazione accettati da backend.</span><span class="sxs-lookup"><span data-stu-id="bc109-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="bc109-124">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bc109-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="bc109-125">-Query</span><span class="sxs-lookup"><span data-stu-id="bc109-125">-Query</span></span>
<span data-ttu-id="bc109-126">Valori dei parametri di query accettati da backend.</span><span class="sxs-lookup"><span data-stu-id="bc109-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="bc109-127">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bc109-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="bc109-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc109-128">CommonParameters</span></span>
<span data-ttu-id="bc109-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc109-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc109-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc109-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc109-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bc109-131">INPUTS</span></span>

### <span data-ttu-id="bc109-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bc109-132">None</span></span>

## <span data-ttu-id="bc109-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc109-133">OUTPUTS</span></span>

### <span data-ttu-id="bc109-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="bc109-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="bc109-135">Note</span><span class="sxs-lookup"><span data-stu-id="bc109-135">NOTES</span></span>

## <span data-ttu-id="bc109-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc109-136">RELATED LINKS</span></span>

[<span data-ttu-id="bc109-137">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="bc109-137">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="bc109-138">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="bc109-138">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="bc109-139">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="bc109-139">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="bc109-140">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="bc109-140">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="bc109-141">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="bc109-141">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
