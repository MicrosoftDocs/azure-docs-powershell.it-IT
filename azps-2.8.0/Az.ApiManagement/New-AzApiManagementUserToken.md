---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementusertoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUserToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUserToken.md
ms.openlocfilehash: 71f4960dce883b809d9ee9c5bc7011d8ab04c5bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675974"
---
# <span data-ttu-id="62516-101">New-AzApiManagementUserToken</span><span class="sxs-lookup"><span data-stu-id="62516-101">New-AzApiManagementUserToken</span></span>

## <span data-ttu-id="62516-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62516-102">SYNOPSIS</span></span>
<span data-ttu-id="62516-103">Genera un token di accesso condiviso per l'utente.</span><span class="sxs-lookup"><span data-stu-id="62516-103">Generates a Shared Access Token for the User.</span></span>

## <span data-ttu-id="62516-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62516-104">SYNTAX</span></span>

```
New-AzApiManagementUserToken -Context <PsApiManagementContext> -UserId <String>
 [-KeyType <PsApiManagementUserKeyType>] [-Expiry <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="62516-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62516-105">DESCRIPTION</span></span>
<span data-ttu-id="62516-106">Il cmdlet **New-AzApiManagementUserToken** genera un token di accesso condiviso per un utente specificato</span><span class="sxs-lookup"><span data-stu-id="62516-106">The cmdlet **New-AzApiManagementUserToken** generates a Shared Access Token for a specified User</span></span>

## <span data-ttu-id="62516-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62516-107">EXAMPLES</span></span>

### <span data-ttu-id="62516-108">Esempio 1: generare un token di accesso condiviso per l'utente git</span><span class="sxs-lookup"><span data-stu-id="62516-108">Example 1 : Generate a Shared Access Token for Git User</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName powershelltest -ServiceName
powershellsdkservice
S D:\github\azure-powershell> $gitAccess=Get-AzApiManagementTenantAccess -Context $context
PS D:\github\azure-powershell> New-AzApiManagementUserToken -Context $context -UserId $gitAccess.Id

UserId      TokenExpiry         KeyType UserToken
------      -----------         ------- ---------
integration 5/3/2019 2:02:34 PM Primary integration&201905031402&zOwopJChWAA6oaqGHMyf7Ol9wUCPcrtdmBmff8c2lcmZk9Y...
```

<span data-ttu-id="62516-109">Questo script ottiene l'utente git configurato nel servizio ApiManagement e genera un token di accesso condiviso usando la chiave primaria valida per 8 ore.</span><span class="sxs-lookup"><span data-stu-id="62516-109">This script get the Git user configured in ApiManagement service and generates a Shared Access Token using the Primary Key valid for 8 hours.</span></span>

## <span data-ttu-id="62516-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62516-110">PARAMETERS</span></span>

### <span data-ttu-id="62516-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="62516-111">-Context</span></span>
<span data-ttu-id="62516-112">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="62516-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="62516-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="62516-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62516-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62516-114">-DefaultProfile</span></span>
<span data-ttu-id="62516-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62516-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62516-116">-Scadenza</span><span class="sxs-lookup"><span data-stu-id="62516-116">-Expiry</span></span>
<span data-ttu-id="62516-117">Scadenza del token.</span><span class="sxs-lookup"><span data-stu-id="62516-117">Expiry of the Token.</span></span>
<span data-ttu-id="62516-118">Se non viene specificato, il token viene creato per scadere dopo 8 ore.</span><span class="sxs-lookup"><span data-stu-id="62516-118">If not specified, the token is created to expire after 8 hours.</span></span>
<span data-ttu-id="62516-119">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="62516-119">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62516-120">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="62516-120">-KeyType</span></span>
<span data-ttu-id="62516-121">Chiave utente da usare per la generazione del token.</span><span class="sxs-lookup"><span data-stu-id="62516-121">User Key to use when generating the Token.</span></span>
<span data-ttu-id="62516-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="62516-122">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserKeyType
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62516-123">-UserId</span><span class="sxs-lookup"><span data-stu-id="62516-123">-UserId</span></span>
<span data-ttu-id="62516-124">Identificatore dell'utente esistente.</span><span class="sxs-lookup"><span data-stu-id="62516-124">Identifier of existing user.</span></span>
<span data-ttu-id="62516-125">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="62516-125">This parameter is required.</span></span>

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

### <span data-ttu-id="62516-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62516-126">CommonParameters</span></span>
<span data-ttu-id="62516-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62516-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62516-128">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62516-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62516-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62516-129">INPUTS</span></span>

### <span data-ttu-id="62516-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="62516-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="62516-131">System. String</span><span class="sxs-lookup"><span data-stu-id="62516-131">System.String</span></span>

### <span data-ttu-id="62516-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUserKeyType</span><span class="sxs-lookup"><span data-stu-id="62516-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserKeyType</span></span>

### <span data-ttu-id="62516-133">System. Nullable ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="62516-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="62516-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62516-134">OUTPUTS</span></span>

### <span data-ttu-id="62516-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUserToken</span><span class="sxs-lookup"><span data-stu-id="62516-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserToken</span></span>

## <span data-ttu-id="62516-136">Note</span><span class="sxs-lookup"><span data-stu-id="62516-136">NOTES</span></span>

## <span data-ttu-id="62516-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62516-137">RELATED LINKS</span></span>
