---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
ms.openlocfilehash: 4453b7fc3e13f4de2632c41cea966fdada1d84f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521480"
---
# <span data-ttu-id="632a6-101">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="632a6-101">New-AzureRmApiManagementBackendCredential</span></span>

## <span data-ttu-id="632a6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="632a6-102">SYNOPSIS</span></span>
<span data-ttu-id="632a6-103">Crea un nuovo contratto di credenziale back-end.</span><span class="sxs-lookup"><span data-stu-id="632a6-103">Creates a new Backend Credential contract.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="632a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="632a6-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="632a6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="632a6-105">DESCRIPTION</span></span>
<span data-ttu-id="632a6-106">Crea un nuovo contratto di credenziale back-end.</span><span class="sxs-lookup"><span data-stu-id="632a6-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="632a6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="632a6-107">EXAMPLES</span></span>

### <span data-ttu-id="632a6-108">Creare un oggetto In-Memory credenziali di backend</span><span class="sxs-lookup"><span data-stu-id="632a6-108">Create a Backend Credentials In-Memory Object</span></span>
```
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}
```

<span data-ttu-id="632a6-109">Crea un contratto di credenziali back-end</span><span class="sxs-lookup"><span data-stu-id="632a6-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="632a6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="632a6-110">PARAMETERS</span></span>

### <span data-ttu-id="632a6-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="632a6-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="632a6-112">Intestazione di autorizzazione usata per il backend.</span><span class="sxs-lookup"><span data-stu-id="632a6-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="632a6-113">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="632a6-113">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632a6-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="632a6-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="632a6-115">Schema di autorizzazione usato per il backend.</span><span class="sxs-lookup"><span data-stu-id="632a6-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="632a6-116">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="632a6-116">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632a6-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="632a6-117">-CertificateThumbprint</span></span>
<span data-ttu-id="632a6-118">Identificazioni personali del certificato client.</span><span class="sxs-lookup"><span data-stu-id="632a6-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="632a6-119">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="632a6-119">This parameter is optional.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632a6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="632a6-120">-DefaultProfile</span></span>
<span data-ttu-id="632a6-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="632a6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="632a6-122">-Intestazione</span><span class="sxs-lookup"><span data-stu-id="632a6-122">-Header</span></span>
<span data-ttu-id="632a6-123">Valori dei parametri di intestazione accettati da backend.</span><span class="sxs-lookup"><span data-stu-id="632a6-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="632a6-124">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="632a6-124">This parameter is optional.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632a6-125">-Query</span><span class="sxs-lookup"><span data-stu-id="632a6-125">-Query</span></span>
<span data-ttu-id="632a6-126">Valori dei parametri di query accettati da backend.</span><span class="sxs-lookup"><span data-stu-id="632a6-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="632a6-127">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="632a6-127">This parameter is optional.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632a6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="632a6-128">CommonParameters</span></span>
<span data-ttu-id="632a6-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="632a6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="632a6-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="632a6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="632a6-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="632a6-131">INPUTS</span></span>

### <span data-ttu-id="632a6-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="632a6-132">None</span></span>
<span data-ttu-id="632a6-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="632a6-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="632a6-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="632a6-134">OUTPUTS</span></span>

### <span data-ttu-id="632a6-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="632a6-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="632a6-136">Note</span><span class="sxs-lookup"><span data-stu-id="632a6-136">NOTES</span></span>

## <span data-ttu-id="632a6-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="632a6-137">RELATED LINKS</span></span>

[<span data-ttu-id="632a6-138">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="632a6-138">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="632a6-139">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="632a6-139">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="632a6-140">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="632a6-140">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="632a6-141">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="632a6-141">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="632a6-142">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="632a6-142">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
