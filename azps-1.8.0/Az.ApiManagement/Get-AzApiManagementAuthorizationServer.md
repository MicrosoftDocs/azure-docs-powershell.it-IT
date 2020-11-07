---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 2624ccad63b2992ef8cae889cea04b849658444e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673648"
---
# <span data-ttu-id="395c1-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="395c1-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="395c1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="395c1-102">SYNOPSIS</span></span>
<span data-ttu-id="395c1-103">Ottiene un server di autorizzazione Gestione API.</span><span class="sxs-lookup"><span data-stu-id="395c1-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="395c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="395c1-104">SYNTAX</span></span>

### <span data-ttu-id="395c1-105">GetAllAuthorizationServers (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="395c1-105">GetAllAuthorizationServers (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="395c1-106">GetByServerId</span><span class="sxs-lookup"><span data-stu-id="395c1-106">GetByServerId</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="395c1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="395c1-107">DESCRIPTION</span></span>
<span data-ttu-id="395c1-108">Il cmdlet **Get-AzApiManagementAuthorizationServer** ottiene tutti i server di autorizzazione di gestione delle API Azure o i server di autorizzazione specificati.</span><span class="sxs-lookup"><span data-stu-id="395c1-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="395c1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="395c1-109">EXAMPLES</span></span>

### <span data-ttu-id="395c1-110">Esempio 1: ottenere tutti i server di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="395c1-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

<span data-ttu-id="395c1-111">Questo comando ottiene tutti i server di autorizzazione per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="395c1-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="395c1-112">Esempio 2: ottenere un server di autorizzazione specificato</span><span class="sxs-lookup"><span data-stu-id="395c1-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="395c1-113">Questo comando ottiene il server di autorizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="395c1-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="395c1-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="395c1-114">PARAMETERS</span></span>

### <span data-ttu-id="395c1-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="395c1-115">-Context</span></span>

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

### <span data-ttu-id="395c1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="395c1-116">-DefaultProfile</span></span>
<span data-ttu-id="395c1-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="395c1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="395c1-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="395c1-118">-ServerId</span></span>
```yaml
Type: System.String
Parameter Sets: GetByServerId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="395c1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="395c1-119">CommonParameters</span></span>
<span data-ttu-id="395c1-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="395c1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="395c1-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="395c1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="395c1-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="395c1-122">INPUTS</span></span>

### <span data-ttu-id="395c1-123">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="395c1-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="395c1-124">System. String</span><span class="sxs-lookup"><span data-stu-id="395c1-124">System.String</span></span>

## <span data-ttu-id="395c1-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="395c1-125">OUTPUTS</span></span>

### <span data-ttu-id="395c1-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="395c1-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="395c1-127">Note</span><span class="sxs-lookup"><span data-stu-id="395c1-127">NOTES</span></span>

## <span data-ttu-id="395c1-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="395c1-128">RELATED LINKS</span></span>

[<span data-ttu-id="395c1-129">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="395c1-129">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="395c1-130">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="395c1-130">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="395c1-131">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="395c1-131">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


