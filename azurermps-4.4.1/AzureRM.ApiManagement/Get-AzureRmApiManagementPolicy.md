---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 16eed643397245fa54b2876430042335762ea048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517259"
---
# <span data-ttu-id="955cc-101">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="955cc-101">Get-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="955cc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="955cc-102">SYNOPSIS</span></span>
<span data-ttu-id="955cc-103">Ottiene il criterio di ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="955cc-103">Gets the specified scope policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="955cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="955cc-104">SYNTAX</span></span>

### <span data-ttu-id="955cc-105">Livello tenant (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="955cc-105">Tenant level (Default)</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="955cc-106">Livello di prodotto</span><span class="sxs-lookup"><span data-stu-id="955cc-106">Product level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="955cc-107">Livello API</span><span class="sxs-lookup"><span data-stu-id="955cc-107">API level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="955cc-108">Livello di operazione</span><span class="sxs-lookup"><span data-stu-id="955cc-108">Operation level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> -OperationId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="955cc-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="955cc-109">DESCRIPTION</span></span>
<span data-ttu-id="955cc-110">Il cmdlet **Get-AzureRmApiManagementPolicy** ottiene il criterio di ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="955cc-110">The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="955cc-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="955cc-111">EXAMPLES</span></span>

### <span data-ttu-id="955cc-112">Esempio 1: ottenere i criteri di livello tenant</span><span class="sxs-lookup"><span data-stu-id="955cc-112">Example 1: Get the tenant level policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="955cc-113">Questo comando consente di ottenere i criteri di livello tenant e di salvarli in un file denominato tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="955cc-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="955cc-114">Esempio 2: ottenere il criterio dell'ambito prodotto</span><span class="sxs-lookup"><span data-stu-id="955cc-114">Example 2: Get the product-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789"
```

<span data-ttu-id="955cc-115">Questo comando ottiene i criteri per l'ambito prodotto</span><span class="sxs-lookup"><span data-stu-id="955cc-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="955cc-116">Esempio 3: ottenere il criterio ambito API</span><span class="sxs-lookup"><span data-stu-id="955cc-116">Example 3: Get the API-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210"
```

<span data-ttu-id="955cc-117">Questo comando ottiene i criteri per l'ambito API.</span><span class="sxs-lookup"><span data-stu-id="955cc-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="955cc-118">Esempio 4: ottenere i criteri di operazione-ambito</span><span class="sxs-lookup"><span data-stu-id="955cc-118">Example 4: Get the operation-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="955cc-119">Questo comando ottiene il criterio ambito operazione.</span><span class="sxs-lookup"><span data-stu-id="955cc-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="955cc-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="955cc-120">PARAMETERS</span></span>

### <span data-ttu-id="955cc-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="955cc-121">-ApiId</span></span>
<span data-ttu-id="955cc-122">Specifica l'identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="955cc-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="955cc-123">Se specifichi questo parametro, il cmdlet restituisce il criterio dell'ambito API.</span><span class="sxs-lookup"><span data-stu-id="955cc-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: API level, Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="955cc-124">-Contesto</span><span class="sxs-lookup"><span data-stu-id="955cc-124">-Context</span></span>
<span data-ttu-id="955cc-125">Specifica un'istanza di **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="955cc-125">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="955cc-126">-Force</span><span class="sxs-lookup"><span data-stu-id="955cc-126">-Force</span></span>
<span data-ttu-id="955cc-127">ps_force</span><span class="sxs-lookup"><span data-stu-id="955cc-127">ps_force</span></span>

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

### <span data-ttu-id="955cc-128">-Format</span><span class="sxs-lookup"><span data-stu-id="955cc-128">-Format</span></span>
<span data-ttu-id="955cc-129">Specifica il formato dei criteri di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="955cc-129">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="955cc-130">Il valore predefinito per questo parametro è "application/vnd. ms-Azure-APIM. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="955cc-130">The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="955cc-131">-OperationId</span><span class="sxs-lookup"><span data-stu-id="955cc-131">-OperationId</span></span>
<span data-ttu-id="955cc-132">Specifica l'identificatore dell'operazione API esistente.</span><span class="sxs-lookup"><span data-stu-id="955cc-132">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="955cc-133">Se specifichi questo parametro con *ApiId* , il cmdlet restituisce i criteri per l'ambito dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="955cc-133">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="955cc-134">-ProductId</span><span class="sxs-lookup"><span data-stu-id="955cc-134">-ProductId</span></span>
<span data-ttu-id="955cc-135">Specifica l'identificatore di un prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="955cc-135">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="955cc-136">Se specifichi questo parametro, il cmdlet restituisce i criteri per l'ambito del prodotto.</span><span class="sxs-lookup"><span data-stu-id="955cc-136">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Product level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="955cc-137">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="955cc-137">-SaveAs</span></span>
<span data-ttu-id="955cc-138">Specifica il percorso del file in cui salvare il risultato.</span><span class="sxs-lookup"><span data-stu-id="955cc-138">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="955cc-139">Se non specifichi questo parametro, il risultato verrà inviato come Sting.</span><span class="sxs-lookup"><span data-stu-id="955cc-139">If you do not specify this parameter the result is pipelined as a sting.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="955cc-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="955cc-140">-Confirm</span></span>
<span data-ttu-id="955cc-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="955cc-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="955cc-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="955cc-142">-WhatIf</span></span>
<span data-ttu-id="955cc-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="955cc-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="955cc-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="955cc-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="955cc-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="955cc-145">-DefaultProfile</span></span>
<span data-ttu-id="955cc-146">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="955cc-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="955cc-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="955cc-147">CommonParameters</span></span>
<span data-ttu-id="955cc-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="955cc-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="955cc-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="955cc-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="955cc-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="955cc-150">INPUTS</span></span>

## <span data-ttu-id="955cc-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="955cc-151">OUTPUTS</span></span>

### <span data-ttu-id="955cc-152">Stringa</span><span class="sxs-lookup"><span data-stu-id="955cc-152">String</span></span>

## <span data-ttu-id="955cc-153">Note</span><span class="sxs-lookup"><span data-stu-id="955cc-153">NOTES</span></span>

## <span data-ttu-id="955cc-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="955cc-154">RELATED LINKS</span></span>

[<span data-ttu-id="955cc-155">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="955cc-155">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="955cc-156">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="955cc-156">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


