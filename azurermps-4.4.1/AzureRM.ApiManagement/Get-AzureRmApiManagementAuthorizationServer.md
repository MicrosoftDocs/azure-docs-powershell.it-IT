---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 3c37376aa475e8b0797d4ff4433ab54a11d2b6bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518444"
---
# <span data-ttu-id="9dad0-101">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="9dad0-101">Get-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="9dad0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9dad0-102">SYNOPSIS</span></span>
<span data-ttu-id="9dad0-103">Ottiene un server di autorizzazione Gestione API.</span><span class="sxs-lookup"><span data-stu-id="9dad0-103">Gets an API Management authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9dad0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9dad0-104">SYNTAX</span></span>

### <span data-ttu-id="9dad0-105">Ottenere tutto il server di autorizzazione (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9dad0-105">Get all authorization server (Default)</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dad0-106">Ottenere per ID</span><span class="sxs-lookup"><span data-stu-id="9dad0-106">Get by Id</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dad0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9dad0-107">DESCRIPTION</span></span>
<span data-ttu-id="9dad0-108">Il cmdlet **Get-AzureRmApiManagementAuthorizationServer** ottiene tutti i server di autorizzazione di gestione delle API Azure o i server di autorizzazione specificati.</span><span class="sxs-lookup"><span data-stu-id="9dad0-108">The **Get-AzureRmApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="9dad0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9dad0-109">EXAMPLES</span></span>

### <span data-ttu-id="9dad0-110">Esempio 1: ottenere tutti i server di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="9dad0-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>Get-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

<span data-ttu-id="9dad0-111">Questo comando ottiene tutti i server di autorizzazione per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="9dad0-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="9dad0-112">Esempio 2: ottenere un server di autorizzazione specificato</span><span class="sxs-lookup"><span data-stu-id="9dad0-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="9dad0-113">Questo comando ottiene il server di autorizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="9dad0-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="9dad0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9dad0-114">PARAMETERS</span></span>

### <span data-ttu-id="9dad0-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="9dad0-115">-Context</span></span>
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

### <span data-ttu-id="9dad0-116">-ServerId</span><span class="sxs-lookup"><span data-stu-id="9dad0-116">-ServerId</span></span>
```yaml
Type: System.String
Parameter Sets: Get by Id
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dad0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dad0-117">-DefaultProfile</span></span>
<span data-ttu-id="9dad0-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9dad0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9dad0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dad0-119">CommonParameters</span></span>
<span data-ttu-id="9dad0-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dad0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dad0-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dad0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dad0-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9dad0-122">INPUTS</span></span>

## <span data-ttu-id="9dad0-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9dad0-123">OUTPUTS</span></span>

### <span data-ttu-id="9dad0-124">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthrozationServer></span><span class="sxs-lookup"><span data-stu-id="9dad0-124">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer></span></span>

## <span data-ttu-id="9dad0-125">Note</span><span class="sxs-lookup"><span data-stu-id="9dad0-125">NOTES</span></span>

## <span data-ttu-id="9dad0-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9dad0-126">RELATED LINKS</span></span>

[<span data-ttu-id="9dad0-127">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="9dad0-127">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="9dad0-128">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="9dad0-128">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="9dad0-129">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="9dad0-129">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


