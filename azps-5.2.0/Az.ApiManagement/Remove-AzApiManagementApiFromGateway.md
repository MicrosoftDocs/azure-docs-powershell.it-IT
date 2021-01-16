---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
ms.openlocfilehash: 506287812f684a778fdb96e750aac34049912b58
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358382"
---
# <span data-ttu-id="2a594-101">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="2a594-101">Remove-AzApiManagementApiFromGateway</span></span>

## <span data-ttu-id="2a594-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2a594-102">SYNOPSIS</span></span>
<span data-ttu-id="2a594-103">Allega un'API a un gateway.</span><span class="sxs-lookup"><span data-stu-id="2a594-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="2a594-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a594-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a594-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a594-105">DESCRIPTION</span></span>
<span data-ttu-id="2a594-106">Il cmdlet **Remove-AzApiManagementApiFromGateway** allega un'API a un gateway.</span><span class="sxs-lookup"><span data-stu-id="2a594-106">The **Remove-AzApiManagementApiFromGateway** cmdlet attaches an API to a gateway.</span></span>

## <span data-ttu-id="2a594-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a594-107">EXAMPLES</span></span>

### <span data-ttu-id="2a594-108">Esempio 1: rimuovere un'API da un gateway</span><span class="sxs-lookup"><span data-stu-id="2a594-108">Example 1: Remove an API from a gateway</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="2a594-109">Questo comando rimuove l'API specificata da un gateway.</span><span class="sxs-lookup"><span data-stu-id="2a594-109">This command removes the specified API from a gateway.</span></span>

## <span data-ttu-id="2a594-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2a594-110">PARAMETERS</span></span>

### <span data-ttu-id="2a594-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2a594-111">-ApiId</span></span>
<span data-ttu-id="2a594-112">Identificatore delle API esistenti da rimuovere dal gateway.</span><span class="sxs-lookup"><span data-stu-id="2a594-112">Identifier of existing APIs to remove from the Gateway.</span></span>
<span data-ttu-id="2a594-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2a594-113">This parameter is required.</span></span>

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

### <span data-ttu-id="2a594-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="2a594-114">-Context</span></span>
<span data-ttu-id="2a594-115">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2a594-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2a594-116">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2a594-116">This parameter is required.</span></span>

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

### <span data-ttu-id="2a594-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a594-117">-DefaultProfile</span></span>
<span data-ttu-id="2a594-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2a594-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a594-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="2a594-119">-GatewayId</span></span>
<span data-ttu-id="2a594-120">Identificatore del gateway esistente per cui rimuovere l'API.</span><span class="sxs-lookup"><span data-stu-id="2a594-120">Identifier of existing Gateway to remove API from.</span></span>
<span data-ttu-id="2a594-121">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2a594-121">This parameter is required.</span></span>

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

### <span data-ttu-id="2a594-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a594-122">-PassThru</span></span>
<span data-ttu-id="2a594-123">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="2a594-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="2a594-124">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2a594-124">This parameter is optional.</span></span>
<span data-ttu-id="2a594-125">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="2a594-125">Default value is false.</span></span>

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

### <span data-ttu-id="2a594-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2a594-126">-Confirm</span></span>
<span data-ttu-id="2a594-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a594-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a594-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a594-128">-WhatIf</span></span>
<span data-ttu-id="2a594-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a594-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a594-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a594-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a594-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a594-131">CommonParameters</span></span>
<span data-ttu-id="2a594-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a594-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a594-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a594-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a594-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2a594-134">INPUTS</span></span>

### <span data-ttu-id="2a594-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2a594-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2a594-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2a594-136">System.String</span></span>

### <span data-ttu-id="2a594-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2a594-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2a594-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a594-138">OUTPUTS</span></span>

### <span data-ttu-id="2a594-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2a594-139">System.Boolean</span></span>

## <span data-ttu-id="2a594-140">Note</span><span class="sxs-lookup"><span data-stu-id="2a594-140">NOTES</span></span>

## <span data-ttu-id="2a594-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a594-141">RELATED LINKS</span></span>
