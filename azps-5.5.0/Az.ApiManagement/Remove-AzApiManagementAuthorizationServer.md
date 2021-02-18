---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 74e876621948587c116f435f70315c04b403c2f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201287"
---
# <span data-ttu-id="1f8ba-101">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="1f8ba-101">Remove-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="1f8ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f8ba-102">SYNOPSIS</span></span>
<span data-ttu-id="1f8ba-103">Rimuove un server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="1f8ba-103">Removes an authorization server.</span></span>

## <span data-ttu-id="1f8ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f8ba-104">SYNTAX</span></span>

```
Remove-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f8ba-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1f8ba-105">DESCRIPTION</span></span>
<span data-ttu-id="1f8ba-106">Il cmdlet **Remove-AzApiManagementAuthorizationServer** rimuove un server di autorizzazione Gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="1f8ba-106">The **Remove-AzApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="1f8ba-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f8ba-107">EXAMPLES</span></span>

### <span data-ttu-id="1f8ba-108">Esempio 1: Rimuovere un server di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="1f8ba-108">Example 1: Remove an authorization server</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "authserverid" -Force
```

<span data-ttu-id="1f8ba-109">Questo comando rimuove il server di autorizzazione gestione API specificato.</span><span class="sxs-lookup"><span data-stu-id="1f8ba-109">This command removes the specified API Management Authorization Server.</span></span>
<span data-ttu-id="1f8ba-110">Poiché è *specificato il* parametro Force, non è necessaria alcuna conferma.</span><span class="sxs-lookup"><span data-stu-id="1f8ba-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="1f8ba-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f8ba-111">PARAMETERS</span></span>

### <span data-ttu-id="1f8ba-112">-Context</span><span class="sxs-lookup"><span data-stu-id="1f8ba-112">-Context</span></span>
<span data-ttu-id="1f8ba-113">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="1f8ba-113">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1f8ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f8ba-114">-DefaultProfile</span></span>
<span data-ttu-id="1f8ba-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f8ba-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f8ba-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f8ba-116">-PassThru</span></span>
<span data-ttu-id="1f8ba-117">passthru</span><span class="sxs-lookup"><span data-stu-id="1f8ba-117">passthru</span></span>

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

### <span data-ttu-id="1f8ba-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="1f8ba-118">-ServerId</span></span>
<span data-ttu-id="1f8ba-119">Specifica l'ID del server di autorizzazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="1f8ba-119">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="1f8ba-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f8ba-120">-Confirm</span></span>
<span data-ttu-id="1f8ba-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f8ba-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f8ba-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f8ba-122">-WhatIf</span></span>
<span data-ttu-id="1f8ba-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f8ba-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f8ba-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f8ba-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f8ba-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f8ba-125">CommonParameters</span></span>
<span data-ttu-id="1f8ba-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f8ba-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f8ba-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1f8ba-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f8ba-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="1f8ba-128">INPUTS</span></span>

### <span data-ttu-id="1f8ba-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1f8ba-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1f8ba-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1f8ba-130">System.String</span></span>

### <span data-ttu-id="1f8ba-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1f8ba-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1f8ba-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f8ba-132">OUTPUTS</span></span>

### <span data-ttu-id="1f8ba-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1f8ba-133">System.Boolean</span></span>

## <span data-ttu-id="1f8ba-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="1f8ba-134">NOTES</span></span>

## <span data-ttu-id="1f8ba-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f8ba-135">RELATED LINKS</span></span>

[<span data-ttu-id="1f8ba-136">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="1f8ba-136">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="1f8ba-137">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="1f8ba-137">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="1f8ba-138">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="1f8ba-138">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


