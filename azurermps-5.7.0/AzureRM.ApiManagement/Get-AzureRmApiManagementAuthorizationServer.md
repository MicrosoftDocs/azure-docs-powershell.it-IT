---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 651ef4c0c44b7e3269eb300dcfa098c39415f77d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686750"
---
# <span data-ttu-id="03a1d-101">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="03a1d-101">Get-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="03a1d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="03a1d-102">SYNOPSIS</span></span>
<span data-ttu-id="03a1d-103">Ottiene un server di autorizzazione Gestione API.</span><span class="sxs-lookup"><span data-stu-id="03a1d-103">Gets an API Management authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03a1d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03a1d-104">SYNTAX</span></span>

### <span data-ttu-id="03a1d-105">GetAllAuthorizationServers (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="03a1d-105">GetAllAuthorizationServers (Default)</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03a1d-106">GetByServerId</span><span class="sxs-lookup"><span data-stu-id="03a1d-106">GetByServerId</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03a1d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03a1d-107">DESCRIPTION</span></span>
<span data-ttu-id="03a1d-108">Il cmdlet **Get-AzureRmApiManagementAuthorizationServer** ottiene tutti i server di autorizzazione di gestione delle API Azure o i server di autorizzazione specificati.</span><span class="sxs-lookup"><span data-stu-id="03a1d-108">The **Get-AzureRmApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="03a1d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03a1d-109">EXAMPLES</span></span>

### <span data-ttu-id="03a1d-110">Esempio 1: ottenere tutti i server di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="03a1d-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

<span data-ttu-id="03a1d-111">Questo comando ottiene tutti i server di autorizzazione per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="03a1d-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="03a1d-112">Esempio 2: ottenere un server di autorizzazione specificato</span><span class="sxs-lookup"><span data-stu-id="03a1d-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="03a1d-113">Questo comando ottiene il server di autorizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="03a1d-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="03a1d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="03a1d-114">PARAMETERS</span></span>

### <span data-ttu-id="03a1d-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="03a1d-115">-Context</span></span>
```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a1d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03a1d-116">-DefaultProfile</span></span>
<span data-ttu-id="03a1d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="03a1d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="03a1d-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="03a1d-118">-ServerId</span></span>
```yaml
Type: String
Parameter Sets: GetByServerId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a1d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03a1d-119">CommonParameters</span></span>
<span data-ttu-id="03a1d-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03a1d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03a1d-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03a1d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03a1d-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="03a1d-122">INPUTS</span></span>

### <span data-ttu-id="03a1d-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="03a1d-123">None</span></span>
<span data-ttu-id="03a1d-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="03a1d-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="03a1d-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03a1d-125">OUTPUTS</span></span>

### <span data-ttu-id="03a1d-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="03a1d-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>
<span data-ttu-id="03a1d-127">Dettagli del server di autorizzazione in un servizio di gestione API specifico.</span><span class="sxs-lookup"><span data-stu-id="03a1d-127">The details of the Authorization Server in a given Api Management service.</span></span>

### <span data-ttu-id="03a1d-128">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthrozationServer></span><span class="sxs-lookup"><span data-stu-id="03a1d-128">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer></span></span>
<span data-ttu-id="03a1d-129">L'elenco di server di autorizzazione in un servizio di gestione API specifico.</span><span class="sxs-lookup"><span data-stu-id="03a1d-129">The list of Authorization Server in a given Api Management service.</span></span>

## <span data-ttu-id="03a1d-130">Note</span><span class="sxs-lookup"><span data-stu-id="03a1d-130">NOTES</span></span>

## <span data-ttu-id="03a1d-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03a1d-131">RELATED LINKS</span></span>

[<span data-ttu-id="03a1d-132">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="03a1d-132">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="03a1d-133">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="03a1d-133">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="03a1d-134">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="03a1d-134">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


