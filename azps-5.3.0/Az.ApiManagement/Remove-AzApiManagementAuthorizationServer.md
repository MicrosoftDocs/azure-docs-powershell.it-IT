---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 74e876621948587c116f435f70315c04b403c2f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382157"
---
# <span data-ttu-id="26a6b-101">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="26a6b-101">Remove-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="26a6b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="26a6b-103">Rimuove un server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="26a6b-103">Removes an authorization server.</span></span>

## <span data-ttu-id="26a6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26a6b-104">SYNTAX</span></span>

```
Remove-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26a6b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26a6b-105">DESCRIPTION</span></span>
<span data-ttu-id="26a6b-106">Il cmdlet **Remove-AzApiManagementAuthorizationServer** rimuove un server di autorizzazione Gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="26a6b-106">The **Remove-AzApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="26a6b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26a6b-107">EXAMPLES</span></span>

### <span data-ttu-id="26a6b-108">Esempio 1: rimuovere un server di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="26a6b-108">Example 1: Remove an authorization server</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "authserverid" -Force
```

<span data-ttu-id="26a6b-109">Questo comando rimuove il server di autorizzazione Gestione API specificato.</span><span class="sxs-lookup"><span data-stu-id="26a6b-109">This command removes the specified API Management Authorization Server.</span></span>
<span data-ttu-id="26a6b-110">Dato che il parametro *Force* è specificato, non è richiesta alcuna conferma.</span><span class="sxs-lookup"><span data-stu-id="26a6b-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="26a6b-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26a6b-111">PARAMETERS</span></span>

### <span data-ttu-id="26a6b-112">-Contesto</span><span class="sxs-lookup"><span data-stu-id="26a6b-112">-Context</span></span>
<span data-ttu-id="26a6b-113">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="26a6b-113">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="26a6b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26a6b-114">-DefaultProfile</span></span>
<span data-ttu-id="26a6b-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26a6b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26a6b-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26a6b-116">-PassThru</span></span>
<span data-ttu-id="26a6b-117">PassThru</span><span class="sxs-lookup"><span data-stu-id="26a6b-117">passthru</span></span>

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

### <span data-ttu-id="26a6b-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="26a6b-118">-ServerId</span></span>
<span data-ttu-id="26a6b-119">Specifica l'ID del server di autorizzazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="26a6b-119">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="26a6b-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="26a6b-120">-Confirm</span></span>
<span data-ttu-id="26a6b-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26a6b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26a6b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26a6b-122">-WhatIf</span></span>
<span data-ttu-id="26a6b-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26a6b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26a6b-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26a6b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26a6b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26a6b-125">CommonParameters</span></span>
<span data-ttu-id="26a6b-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26a6b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26a6b-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26a6b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26a6b-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26a6b-128">INPUTS</span></span>

### <span data-ttu-id="26a6b-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="26a6b-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="26a6b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="26a6b-130">System.String</span></span>

### <span data-ttu-id="26a6b-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="26a6b-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="26a6b-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26a6b-132">OUTPUTS</span></span>

### <span data-ttu-id="26a6b-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26a6b-133">System.Boolean</span></span>

## <span data-ttu-id="26a6b-134">Note</span><span class="sxs-lookup"><span data-stu-id="26a6b-134">NOTES</span></span>

## <span data-ttu-id="26a6b-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26a6b-135">RELATED LINKS</span></span>

[<span data-ttu-id="26a6b-136">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="26a6b-136">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="26a6b-137">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="26a6b-137">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="26a6b-138">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="26a6b-138">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


