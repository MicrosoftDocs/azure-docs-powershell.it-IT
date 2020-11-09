---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
ms.openlocfilehash: a51bd7aed5ca8793a921c2cde7729c5280df44b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310986"
---
# <span data-ttu-id="95ae8-101">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="95ae8-101">Remove-AzApiManagementPolicy</span></span>

## <span data-ttu-id="95ae8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="95ae8-102">SYNOPSIS</span></span>
<span data-ttu-id="95ae8-103">Rimuove i criteri di gestione delle API da un ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="95ae8-103">Removes the API Management policy from a specified scope.</span></span>

## <span data-ttu-id="95ae8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95ae8-104">SYNTAX</span></span>

### <span data-ttu-id="95ae8-105">RemoveTenantLevel (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="95ae8-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95ae8-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="95ae8-106">RemoveProductLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95ae8-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="95ae8-107">RemoveApiLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95ae8-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="95ae8-108">RemoveOperationLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95ae8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95ae8-109">DESCRIPTION</span></span>
<span data-ttu-id="95ae8-110">Il cmdlet **Remove-AzApiManagementPolicy** rimuove i criteri di gestione delle API dall'ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="95ae8-110">The **Remove-AzApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="95ae8-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95ae8-111">EXAMPLES</span></span>

### <span data-ttu-id="95ae8-112">Esempio 1: rimuovere i criteri di livello tenant</span><span class="sxs-lookup"><span data-stu-id="95ae8-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="95ae8-113">Questo comando rimuove i criteri di livello tenant dalla gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="95ae8-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="95ae8-114">Esempio 2: rimuovere il criterio dell'ambito prodotto</span><span class="sxs-lookup"><span data-stu-id="95ae8-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="95ae8-115">Questo comando rimuove i criteri per l'ambito prodotto dalla gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="95ae8-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="95ae8-116">Esempio 3: rimuovere il criterio dell'ambito API</span><span class="sxs-lookup"><span data-stu-id="95ae8-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="95ae8-117">Questo comando rimuove i criteri per l'ambito API dalla gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="95ae8-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="95ae8-118">Esempio 4: rimuovere i criteri per l'ambito dell'operazione</span><span class="sxs-lookup"><span data-stu-id="95ae8-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="95ae8-119">Questo comando rimuove i criteri per l'ambito delle operazioni dalla gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="95ae8-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="95ae8-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="95ae8-120">PARAMETERS</span></span>

### <span data-ttu-id="95ae8-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="95ae8-121">-ApiId</span></span>
<span data-ttu-id="95ae8-122">Specifica l'identificatore di un'API esistente.</span><span class="sxs-lookup"><span data-stu-id="95ae8-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="95ae8-123">Se specifichi questo parametro, il cmdlet rimuove il criterio dell'ambito API.</span><span class="sxs-lookup"><span data-stu-id="95ae8-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

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

### <span data-ttu-id="95ae8-124">-Contesto</span><span class="sxs-lookup"><span data-stu-id="95ae8-124">-Context</span></span>
<span data-ttu-id="95ae8-125">Specifica l'istanza dell'oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="95ae8-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="95ae8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95ae8-126">-DefaultProfile</span></span>
<span data-ttu-id="95ae8-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="95ae8-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95ae8-128">-OperationId</span><span class="sxs-lookup"><span data-stu-id="95ae8-128">-OperationId</span></span>
<span data-ttu-id="95ae8-129">Specifica l'identificatore di un'operazione esistente.</span><span class="sxs-lookup"><span data-stu-id="95ae8-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="95ae8-130">Se specifichi questo parametro con il parametro *ApiId* , questo cmdlet rimuove i criteri per l'ambito dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="95ae8-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

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

### <span data-ttu-id="95ae8-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95ae8-131">-PassThru</span></span>
<span data-ttu-id="95ae8-132">Indica che questo cmdlet restituisce un valore di $True, se ha esito positivo o un valore di $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="95ae8-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="95ae8-133">-ProductId</span><span class="sxs-lookup"><span data-stu-id="95ae8-133">-ProductId</span></span>
<span data-ttu-id="95ae8-134">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="95ae8-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="95ae8-135">Se specifichi questo parametro, il cmdlet rimuove i criteri per l'ambito del prodotto.</span><span class="sxs-lookup"><span data-stu-id="95ae8-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

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

### <span data-ttu-id="95ae8-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="95ae8-136">-Confirm</span></span>
<span data-ttu-id="95ae8-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95ae8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95ae8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95ae8-138">-WhatIf</span></span>
<span data-ttu-id="95ae8-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95ae8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95ae8-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95ae8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95ae8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95ae8-141">CommonParameters</span></span>
<span data-ttu-id="95ae8-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95ae8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95ae8-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95ae8-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95ae8-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="95ae8-144">INPUTS</span></span>

### <span data-ttu-id="95ae8-145">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="95ae8-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="95ae8-146">System. String</span><span class="sxs-lookup"><span data-stu-id="95ae8-146">System.String</span></span>

### <span data-ttu-id="95ae8-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="95ae8-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="95ae8-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95ae8-148">OUTPUTS</span></span>

### <span data-ttu-id="95ae8-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="95ae8-149">System.Boolean</span></span>

## <span data-ttu-id="95ae8-150">Note</span><span class="sxs-lookup"><span data-stu-id="95ae8-150">NOTES</span></span>

## <span data-ttu-id="95ae8-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95ae8-151">RELATED LINKS</span></span>

[<span data-ttu-id="95ae8-152">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="95ae8-152">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="95ae8-153">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="95ae8-153">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


