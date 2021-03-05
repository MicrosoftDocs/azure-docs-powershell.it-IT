---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
ms.openlocfilehash: aecf4982b6a48ac5afca1379e1f920cfa3d6e267
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979037"
---
# <span data-ttu-id="24d54-101">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="24d54-101">Remove-AzApiManagementPolicy</span></span>

## <span data-ttu-id="24d54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24d54-102">SYNOPSIS</span></span>
<span data-ttu-id="24d54-103">Rimuove i criteri di gestione delle API da un ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="24d54-103">Removes the API Management policy from a specified scope.</span></span>

## <span data-ttu-id="24d54-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24d54-104">SYNTAX</span></span>

### <span data-ttu-id="24d54-105">RemoveTenantLevel (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="24d54-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24d54-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="24d54-106">RemoveProductLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24d54-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="24d54-107">RemoveApiLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24d54-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="24d54-108">RemoveOperationLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24d54-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="24d54-109">DESCRIPTION</span></span>
<span data-ttu-id="24d54-110">Il cmdlet **Remove-AzApiManagementPolicy** rimuove il criterio di gestione delle API dall'ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="24d54-110">The **Remove-AzApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="24d54-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24d54-111">EXAMPLES</span></span>

### <span data-ttu-id="24d54-112">Esempio 1: Rimuovere i criteri a livello di tenant</span><span class="sxs-lookup"><span data-stu-id="24d54-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="24d54-113">Questo comando rimuove i criteri a livello di tenant da Gestione API.</span><span class="sxs-lookup"><span data-stu-id="24d54-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="24d54-114">Esempio 2: Rimuovere i criteri di ambito del prodotto</span><span class="sxs-lookup"><span data-stu-id="24d54-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="24d54-115">Questo comando rimuove i criteri di ambito del prodotto da Gestione API.</span><span class="sxs-lookup"><span data-stu-id="24d54-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="24d54-116">Esempio 3: Rimuovere il criterio di ambito API</span><span class="sxs-lookup"><span data-stu-id="24d54-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="24d54-117">Questo comando rimuove i criteri di ambito API da Gestione API.</span><span class="sxs-lookup"><span data-stu-id="24d54-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="24d54-118">Esempio 4: Rimuovere il criterio di ambito delle operazioni</span><span class="sxs-lookup"><span data-stu-id="24d54-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="24d54-119">Questo comando rimuove il criterio di ambito dell'operazione da Gestione API.</span><span class="sxs-lookup"><span data-stu-id="24d54-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="24d54-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24d54-120">PARAMETERS</span></span>

### <span data-ttu-id="24d54-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="24d54-121">-ApiId</span></span>
<span data-ttu-id="24d54-122">Specifica l'identificatore di un'API esistente.</span><span class="sxs-lookup"><span data-stu-id="24d54-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="24d54-123">Se si specifica questo parametro, il cmdlet rimuove il criterio di ambito API.</span><span class="sxs-lookup"><span data-stu-id="24d54-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveApiLevel, RemoveOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24d54-124">-Context</span><span class="sxs-lookup"><span data-stu-id="24d54-124">-Context</span></span>
<span data-ttu-id="24d54-125">Specifica l'istanza **dell'oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="24d54-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="24d54-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24d54-126">-DefaultProfile</span></span>
<span data-ttu-id="24d54-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24d54-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24d54-128">-OperationId</span><span class="sxs-lookup"><span data-stu-id="24d54-128">-OperationId</span></span>
<span data-ttu-id="24d54-129">Specifica l'identificatore di un'operazione esistente.</span><span class="sxs-lookup"><span data-stu-id="24d54-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="24d54-130">Se si specifica questo parametro con il parametro *ApiId,* questo cmdlet rimuove i criteri di ambito dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="24d54-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24d54-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24d54-131">-PassThru</span></span>
<span data-ttu-id="24d54-132">Indica che questo cmdlet restituisce il valore $True, se ha esito positivo, o un valore di $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="24d54-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="24d54-133">-ProductId</span><span class="sxs-lookup"><span data-stu-id="24d54-133">-ProductId</span></span>
<span data-ttu-id="24d54-134">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="24d54-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="24d54-135">Se si specifica questo parametro, il cmdlet rimuove i criteri di ambito del prodotto.</span><span class="sxs-lookup"><span data-stu-id="24d54-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24d54-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24d54-136">-Confirm</span></span>
<span data-ttu-id="24d54-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24d54-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24d54-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24d54-138">-WhatIf</span></span>
<span data-ttu-id="24d54-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24d54-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24d54-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24d54-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24d54-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d54-141">CommonParameters</span></span>
<span data-ttu-id="24d54-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24d54-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d54-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="24d54-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d54-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="24d54-144">INPUTS</span></span>

### <span data-ttu-id="24d54-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="24d54-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="24d54-146">System.String</span><span class="sxs-lookup"><span data-stu-id="24d54-146">System.String</span></span>

### <span data-ttu-id="24d54-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="24d54-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="24d54-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24d54-148">OUTPUTS</span></span>

### <span data-ttu-id="24d54-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="24d54-149">System.Boolean</span></span>

## <span data-ttu-id="24d54-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="24d54-150">NOTES</span></span>

## <span data-ttu-id="24d54-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24d54-151">RELATED LINKS</span></span>

[<span data-ttu-id="24d54-152">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="24d54-152">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="24d54-153">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="24d54-153">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


