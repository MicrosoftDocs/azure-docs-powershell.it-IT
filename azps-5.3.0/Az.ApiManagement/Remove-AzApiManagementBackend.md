---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: 073b32936be1e1614e495ca680a250498742ba66
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382168"
---
# <span data-ttu-id="8a079-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8a079-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="8a079-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a079-102">SYNOPSIS</span></span>
<span data-ttu-id="8a079-103">Rimuove un backend.</span><span class="sxs-lookup"><span data-stu-id="8a079-103">Removes a Backend.</span></span>

## <span data-ttu-id="8a079-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a079-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a079-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a079-105">DESCRIPTION</span></span>
<span data-ttu-id="8a079-106">Rimuove un backend specificato dall'identificatore dalla gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="8a079-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="8a079-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a079-107">EXAMPLES</span></span>

### <span data-ttu-id="8a079-108">Esempio 1: rimuovere il backend 123</span><span class="sxs-lookup"><span data-stu-id="8a079-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="8a079-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a079-109">PARAMETERS</span></span>

### <span data-ttu-id="8a079-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="8a079-110">-BackendId</span></span>
<span data-ttu-id="8a079-111">Identificatore del backend esistente.</span><span class="sxs-lookup"><span data-stu-id="8a079-111">Identifier of existing backend.</span></span>
<span data-ttu-id="8a079-112">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8a079-112">This parameter is required.</span></span>

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

### <span data-ttu-id="8a079-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="8a079-113">-Context</span></span>
<span data-ttu-id="8a079-114">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8a079-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8a079-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8a079-115">This parameter is required.</span></span>

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

### <span data-ttu-id="8a079-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a079-116">-DefaultProfile</span></span>
<span data-ttu-id="8a079-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8a079-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a079-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a079-118">-PassThru</span></span>
<span data-ttu-id="8a079-119">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="8a079-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="8a079-120">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8a079-120">This parameter is optional.</span></span>
<span data-ttu-id="8a079-121">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="8a079-121">Default value is false.</span></span>

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

### <span data-ttu-id="8a079-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8a079-122">-Confirm</span></span>
<span data-ttu-id="8a079-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a079-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a079-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a079-124">-WhatIf</span></span>
<span data-ttu-id="8a079-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a079-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a079-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a079-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a079-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a079-127">CommonParameters</span></span>
<span data-ttu-id="8a079-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a079-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a079-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a079-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a079-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a079-130">INPUTS</span></span>

### <span data-ttu-id="8a079-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8a079-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8a079-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8a079-132">System.String</span></span>

### <span data-ttu-id="8a079-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8a079-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8a079-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a079-134">OUTPUTS</span></span>

### <span data-ttu-id="8a079-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8a079-135">System.Boolean</span></span>

## <span data-ttu-id="8a079-136">Note</span><span class="sxs-lookup"><span data-stu-id="8a079-136">NOTES</span></span>

## <span data-ttu-id="8a079-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a079-137">RELATED LINKS</span></span>

[<span data-ttu-id="8a079-138">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8a079-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="8a079-139">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8a079-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="8a079-140">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="8a079-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="8a079-141">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="8a079-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="8a079-142">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8a079-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)
