---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 31b38d07aea51ad1e6bd097cc0c9f7f342e1bfb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514608"
---
# <span data-ttu-id="d0eb3-101">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d0eb3-101">Get-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="d0eb3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d0eb3-102">SYNOPSIS</span></span>
<span data-ttu-id="d0eb3-103">Ottiene il criterio di ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="d0eb3-103">Gets the specified scope policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0eb3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0eb3-104">SYNTAX</span></span>

### <span data-ttu-id="d0eb3-105">GetTenantLevel (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d0eb3-105">GetTenantLevel (Default)</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0eb3-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="d0eb3-106">GetProductLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0eb3-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="d0eb3-107">GetApiLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0eb3-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="d0eb3-108">GetOperationLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> -OperationId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0eb3-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0eb3-109">DESCRIPTION</span></span>
<span data-ttu-id="d0eb3-110">Il cmdlet **Get-AzureRmApiManagementPolicy** ottiene il criterio di ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="d0eb3-110">The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="d0eb3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0eb3-111">EXAMPLES</span></span>

### <span data-ttu-id="d0eb3-112">Esempio 1: ottenere i criteri di livello tenant</span><span class="sxs-lookup"><span data-stu-id="d0eb3-112">Example 1: Get the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="d0eb3-113">Questo comando consente di ottenere i criteri di livello tenant e di salvarli in un file denominato tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="d0eb3-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="d0eb3-114">Esempio 2: ottenere il criterio dell'ambito prodotto</span><span class="sxs-lookup"><span data-stu-id="d0eb3-114">Example 2: Get the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="d0eb3-115">Questo comando ottiene i criteri per l'ambito prodotto</span><span class="sxs-lookup"><span data-stu-id="d0eb3-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="d0eb3-116">Esempio 3: ottenere il criterio ambito API</span><span class="sxs-lookup"><span data-stu-id="d0eb3-116">Example 3: Get the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="d0eb3-117">Questo comando ottiene i criteri per l'ambito API.</span><span class="sxs-lookup"><span data-stu-id="d0eb3-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="d0eb3-118">Esempio 4: ottenere i criteri di operazione-ambito</span><span class="sxs-lookup"><span data-stu-id="d0eb3-118">Example 4: Get the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="d0eb3-119">Questo comando ottiene il criterio ambito operazione.</span><span class="sxs-lookup"><span data-stu-id="d0eb3-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="d0eb3-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d0eb3-120">PARAMETERS</span></span>

### <span data-ttu-id="d0eb3-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d0eb3-121">-ApiId</span></span>
<span data-ttu-id="d0eb3-122">Specifica l'identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="d0eb3-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="d0eb3-123">Se specifichi questo parametro, il cmdlet restituisce il criterio dell'ambito API.</span><span class="sxs-lookup"><span data-stu-id="d0eb3-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0eb3-124">-Contesto</span><span class="sxs-lookup"><span data-stu-id="d0eb3-124">-Context</span></span>
<span data-ttu-id="d0eb3-125">Specifica un'istanza di **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="d0eb3-125">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0eb3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0eb3-126">-DefaultProfile</span></span>
<span data-ttu-id="d0eb3-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d0eb3-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0eb3-128">-Force</span><span class="sxs-lookup"><span data-stu-id="d0eb3-128">-Force</span></span>
<span data-ttu-id="d0eb3-129">ps_force</span><span class="sxs-lookup"><span data-stu-id="d0eb3-129">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0eb3-130">-Format</span><span class="sxs-lookup"><span data-stu-id="d0eb3-130">-Format</span></span>
<span data-ttu-id="d0eb3-131">Specifica il formato dei criteri di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="d0eb3-131">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="d0eb3-132">Il valore predefinito per questo parametro è "application/vnd. ms-Azure-APIM. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="d0eb3-132">The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0eb3-133">-OperationId</span><span class="sxs-lookup"><span data-stu-id="d0eb3-133">-OperationId</span></span>
<span data-ttu-id="d0eb3-134">Specifica l'identificatore dell'operazione API esistente.</span><span class="sxs-lookup"><span data-stu-id="d0eb3-134">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="d0eb3-135">Se specifichi questo parametro con *ApiId* , il cmdlet restituisce i criteri per l'ambito dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d0eb3-135">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: GetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0eb3-136">-ProductId</span><span class="sxs-lookup"><span data-stu-id="d0eb3-136">-ProductId</span></span>
<span data-ttu-id="d0eb3-137">Specifica l'identificatore di un prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="d0eb3-137">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="d0eb3-138">Se specifichi questo parametro, il cmdlet restituisce i criteri per l'ambito del prodotto.</span><span class="sxs-lookup"><span data-stu-id="d0eb3-138">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: GetProductLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0eb3-139">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="d0eb3-139">-SaveAs</span></span>
<span data-ttu-id="d0eb3-140">Specifica il percorso del file in cui salvare il risultato.</span><span class="sxs-lookup"><span data-stu-id="d0eb3-140">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="d0eb3-141">Se non specifichi questo parametro, il risultato verrà inviato come Sting.</span><span class="sxs-lookup"><span data-stu-id="d0eb3-141">If you do not specify this parameter the result is pipelined as a sting.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0eb3-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d0eb3-142">-Confirm</span></span>
<span data-ttu-id="d0eb3-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0eb3-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0eb3-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0eb3-144">-WhatIf</span></span>
<span data-ttu-id="d0eb3-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0eb3-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0eb3-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0eb3-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0eb3-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0eb3-147">CommonParameters</span></span>
<span data-ttu-id="d0eb3-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0eb3-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0eb3-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0eb3-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0eb3-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d0eb3-150">INPUTS</span></span>

### <span data-ttu-id="d0eb3-151">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d0eb3-151">None</span></span>
<span data-ttu-id="d0eb3-152">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d0eb3-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d0eb3-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0eb3-153">OUTPUTS</span></span>

### <span data-ttu-id="d0eb3-154">Stringa</span><span class="sxs-lookup"><span data-stu-id="d0eb3-154">String</span></span>

## <span data-ttu-id="d0eb3-155">Note</span><span class="sxs-lookup"><span data-stu-id="d0eb3-155">NOTES</span></span>

## <span data-ttu-id="d0eb3-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0eb3-156">RELATED LINKS</span></span>

[<span data-ttu-id="d0eb3-157">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d0eb3-157">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="d0eb3-158">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d0eb3-158">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


