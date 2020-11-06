---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 1066598a9e255cecbf7238208b5f06f74d88511e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513983"
---
# <span data-ttu-id="7ccb4-101">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7ccb4-101">Remove-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="7ccb4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7ccb4-102">SYNOPSIS</span></span>
<span data-ttu-id="7ccb4-103">Rimuove i criteri di gestione delle API da un ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-103">Removes the API Management policy from a specified scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ccb4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ccb4-104">SYNTAX</span></span>

### <span data-ttu-id="7ccb4-105">RemoveTenantLevel (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7ccb4-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ccb4-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="7ccb4-106">RemoveProductLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ccb4-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="7ccb4-107">RemoveApiLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ccb4-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="7ccb4-108">RemoveOperationLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ccb4-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ccb4-109">DESCRIPTION</span></span>
<span data-ttu-id="7ccb4-110">Il cmdlet **Remove-AzureRmApiManagementPolicy** rimuove i criteri di gestione delle API dall'ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-110">The **Remove-AzureRmApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="7ccb4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ccb4-111">EXAMPLES</span></span>

### <span data-ttu-id="7ccb4-112">Esempio 1: rimuovere i criteri di livello tenant</span><span class="sxs-lookup"><span data-stu-id="7ccb4-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="7ccb4-113">Questo comando rimuove i criteri di livello tenant dalla gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="7ccb4-114">Esempio 2: rimuovere il criterio dell'ambito prodotto</span><span class="sxs-lookup"><span data-stu-id="7ccb4-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="7ccb4-115">Questo comando rimuove i criteri per l'ambito prodotto dalla gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="7ccb4-116">Esempio 3: rimuovere il criterio dell'ambito API</span><span class="sxs-lookup"><span data-stu-id="7ccb4-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="7ccb4-117">Questo comando rimuove i criteri per l'ambito API dalla gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="7ccb4-118">Esempio 4: rimuovere i criteri per l'ambito dell'operazione</span><span class="sxs-lookup"><span data-stu-id="7ccb4-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="7ccb4-119">Questo comando rimuove i criteri per l'ambito delle operazioni dalla gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="7ccb4-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7ccb4-120">PARAMETERS</span></span>

### <span data-ttu-id="7ccb4-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7ccb4-121">-ApiId</span></span>
<span data-ttu-id="7ccb4-122">Specifica l'identificatore di un'API esistente.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="7ccb4-123">Se specifichi questo parametro, il cmdlet rimuove il criterio dell'ambito API.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

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

### <span data-ttu-id="7ccb4-124">-Contesto</span><span class="sxs-lookup"><span data-stu-id="7ccb4-124">-Context</span></span>
<span data-ttu-id="7ccb4-125">Specifica l'istanza dell'oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="7ccb4-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7ccb4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ccb4-126">-DefaultProfile</span></span>
<span data-ttu-id="7ccb4-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ccb4-128">-OperationId</span><span class="sxs-lookup"><span data-stu-id="7ccb4-128">-OperationId</span></span>
<span data-ttu-id="7ccb4-129">Specifica l'identificatore di un'operazione esistente.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="7ccb4-130">Se specifichi questo parametro con il parametro *ApiId* , questo cmdlet rimuove i criteri per l'ambito dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

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

### <span data-ttu-id="7ccb4-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ccb4-131">-PassThru</span></span>
<span data-ttu-id="7ccb4-132">Indica che questo cmdlet restituisce un valore di $True, se ha esito positivo o un valore di $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="7ccb4-133">-ProductId</span><span class="sxs-lookup"><span data-stu-id="7ccb4-133">-ProductId</span></span>
<span data-ttu-id="7ccb4-134">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="7ccb4-135">Se specifichi questo parametro, il cmdlet rimuove i criteri per l'ambito del prodotto.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

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

### <span data-ttu-id="7ccb4-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7ccb4-136">-Confirm</span></span>
<span data-ttu-id="7ccb4-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ccb4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ccb4-138">-WhatIf</span></span>
<span data-ttu-id="7ccb4-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ccb4-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ccb4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ccb4-141">CommonParameters</span></span>
<span data-ttu-id="7ccb4-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ccb4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ccb4-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ccb4-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ccb4-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7ccb4-144">INPUTS</span></span>

### <span data-ttu-id="7ccb4-145">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7ccb4-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7ccb4-146">System. String</span><span class="sxs-lookup"><span data-stu-id="7ccb4-146">System.String</span></span>

### <span data-ttu-id="7ccb4-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7ccb4-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7ccb4-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ccb4-148">OUTPUTS</span></span>

### <span data-ttu-id="7ccb4-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7ccb4-149">System.Boolean</span></span>

## <span data-ttu-id="7ccb4-150">Note</span><span class="sxs-lookup"><span data-stu-id="7ccb4-150">NOTES</span></span>

## <span data-ttu-id="7ccb4-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ccb4-151">RELATED LINKS</span></span>

[<span data-ttu-id="7ccb4-152">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7ccb4-152">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="7ccb4-153">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7ccb4-153">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


