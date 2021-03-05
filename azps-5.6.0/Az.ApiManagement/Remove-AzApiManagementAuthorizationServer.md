---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 8cbb9afc37242330bc76b7413033dc41cbd61cd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973005"
---
# <span data-ttu-id="85310-101">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="85310-101">Remove-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="85310-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85310-102">SYNOPSIS</span></span>
<span data-ttu-id="85310-103">Rimuove un server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="85310-103">Removes an authorization server.</span></span>

## <span data-ttu-id="85310-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85310-104">SYNTAX</span></span>

```
Remove-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85310-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="85310-105">DESCRIPTION</span></span>
<span data-ttu-id="85310-106">Il cmdlet **Remove-AzApiManagementAuthorizationServer** rimuove un server di autorizzazione Gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="85310-106">The **Remove-AzApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="85310-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85310-107">EXAMPLES</span></span>

### <span data-ttu-id="85310-108">Esempio 1: Rimuovere un server di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="85310-108">Example 1: Remove an authorization server</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "authserverid" -Force
```

<span data-ttu-id="85310-109">Questo comando rimuove il server di autorizzazione gestione API specificato.</span><span class="sxs-lookup"><span data-stu-id="85310-109">This command removes the specified API Management Authorization Server.</span></span>
<span data-ttu-id="85310-110">Poiché il *parametro Force* è specificato, non è necessaria alcuna conferma.</span><span class="sxs-lookup"><span data-stu-id="85310-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="85310-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85310-111">PARAMETERS</span></span>

### <span data-ttu-id="85310-112">-Context</span><span class="sxs-lookup"><span data-stu-id="85310-112">-Context</span></span>
<span data-ttu-id="85310-113">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="85310-113">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85310-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85310-114">-DefaultProfile</span></span>
<span data-ttu-id="85310-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85310-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85310-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85310-116">-PassThru</span></span>
<span data-ttu-id="85310-117">passthru</span><span class="sxs-lookup"><span data-stu-id="85310-117">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85310-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="85310-118">-ServerId</span></span>
<span data-ttu-id="85310-119">Specifica l'ID del server di autorizzazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="85310-119">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="85310-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85310-120">-Confirm</span></span>
<span data-ttu-id="85310-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85310-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85310-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85310-122">-WhatIf</span></span>
<span data-ttu-id="85310-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85310-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85310-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85310-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85310-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85310-125">CommonParameters</span></span>
<span data-ttu-id="85310-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85310-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85310-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="85310-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85310-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="85310-128">INPUTS</span></span>

### <span data-ttu-id="85310-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="85310-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="85310-130">System.String</span><span class="sxs-lookup"><span data-stu-id="85310-130">System.String</span></span>

### <span data-ttu-id="85310-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="85310-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="85310-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85310-132">OUTPUTS</span></span>

### <span data-ttu-id="85310-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="85310-133">System.Boolean</span></span>

## <span data-ttu-id="85310-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="85310-134">NOTES</span></span>

## <span data-ttu-id="85310-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85310-135">RELATED LINKS</span></span>

[<span data-ttu-id="85310-136">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="85310-136">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="85310-137">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="85310-137">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="85310-138">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="85310-138">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


