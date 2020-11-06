---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: fcf88fcb9b54adec01b8a04b50f557b6a74e7ca8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507788"
---
# <span data-ttu-id="b660e-101">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b660e-101">Get-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="b660e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b660e-102">SYNOPSIS</span></span>
<span data-ttu-id="b660e-103">Ottiene il criterio di ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="b660e-103">Gets the specified scope policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b660e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b660e-104">SYNTAX</span></span>

### <span data-ttu-id="b660e-105">GetTenantLevel (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b660e-105">GetTenantLevel (Default)</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b660e-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="b660e-106">GetProductLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b660e-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="b660e-107">GetApiLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b660e-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="b660e-108">GetOperationLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b660e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b660e-109">DESCRIPTION</span></span>
<span data-ttu-id="b660e-110">Il cmdlet **Get-AzureRmApiManagementPolicy** ottiene il criterio di ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="b660e-110">The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="b660e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b660e-111">EXAMPLES</span></span>

### <span data-ttu-id="b660e-112">Esempio 1: ottenere i criteri di livello tenant</span><span class="sxs-lookup"><span data-stu-id="b660e-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="b660e-113">Questo comando consente di ottenere i criteri di livello tenant e di salvarli in un file denominato tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="b660e-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="b660e-114">Esempio 2: ottenere il criterio dell'ambito prodotto</span><span class="sxs-lookup"><span data-stu-id="b660e-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="b660e-115">Questo comando ottiene i criteri per l'ambito prodotto</span><span class="sxs-lookup"><span data-stu-id="b660e-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="b660e-116">Esempio 3: ottenere il criterio ambito API</span><span class="sxs-lookup"><span data-stu-id="b660e-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="b660e-117">Questo comando ottiene i criteri per l'ambito API.</span><span class="sxs-lookup"><span data-stu-id="b660e-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="b660e-118">Esempio 4: ottenere i criteri di operazione-ambito</span><span class="sxs-lookup"><span data-stu-id="b660e-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="b660e-119">Questo comando ottiene il criterio ambito operazione.</span><span class="sxs-lookup"><span data-stu-id="b660e-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="b660e-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b660e-120">PARAMETERS</span></span>

### <span data-ttu-id="b660e-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b660e-121">-ApiId</span></span>
<span data-ttu-id="b660e-122">Specifica l'identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="b660e-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="b660e-123">Se specifichi questo parametro, il cmdlet restituisce il criterio dell'ambito API.</span><span class="sxs-lookup"><span data-stu-id="b660e-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b660e-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="b660e-124">-ApiRevision</span></span>
<span data-ttu-id="b660e-125">Identificatore della revisione API.</span><span class="sxs-lookup"><span data-stu-id="b660e-125">Identifier of API Revision.</span></span> <span data-ttu-id="b660e-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b660e-126">This parameter is optional.</span></span> <span data-ttu-id="b660e-127">Se non specificato, il criterio verrà recuperato dalla revisione API attualmente attiva.</span><span class="sxs-lookup"><span data-stu-id="b660e-127">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b660e-128">-Contesto</span><span class="sxs-lookup"><span data-stu-id="b660e-128">-Context</span></span>
<span data-ttu-id="b660e-129">Specifica un'istanza di **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="b660e-129">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="b660e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b660e-130">-DefaultProfile</span></span>
<span data-ttu-id="b660e-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b660e-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b660e-132">-Force</span><span class="sxs-lookup"><span data-stu-id="b660e-132">-Force</span></span>
<span data-ttu-id="b660e-133">ps_force</span><span class="sxs-lookup"><span data-stu-id="b660e-133">ps_force</span></span>

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

### <span data-ttu-id="b660e-134">-Format</span><span class="sxs-lookup"><span data-stu-id="b660e-134">-Format</span></span>
<span data-ttu-id="b660e-135">Specifica il formato dei criteri di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="b660e-135">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="b660e-136">Il valore predefinito per questo parametro è "application/vnd. ms-Azure-APIM. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="b660e-136">The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="b660e-137">-OperationId</span><span class="sxs-lookup"><span data-stu-id="b660e-137">-OperationId</span></span>
<span data-ttu-id="b660e-138">Specifica l'identificatore dell'operazione API esistente.</span><span class="sxs-lookup"><span data-stu-id="b660e-138">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="b660e-139">Se specifichi questo parametro con *ApiId* , il cmdlet restituisce i criteri per l'ambito dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b660e-139">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b660e-140">-ProductId</span><span class="sxs-lookup"><span data-stu-id="b660e-140">-ProductId</span></span>
<span data-ttu-id="b660e-141">Specifica l'identificatore di un prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="b660e-141">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="b660e-142">Se specifichi questo parametro, il cmdlet restituisce i criteri per l'ambito del prodotto.</span><span class="sxs-lookup"><span data-stu-id="b660e-142">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b660e-143">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="b660e-143">-SaveAs</span></span>
<span data-ttu-id="b660e-144">Specifica il percorso del file in cui salvare il risultato.</span><span class="sxs-lookup"><span data-stu-id="b660e-144">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="b660e-145">Se non specifichi questo parametro, il risultato verrà inviato come Sting.</span><span class="sxs-lookup"><span data-stu-id="b660e-145">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="b660e-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b660e-146">-Confirm</span></span>
<span data-ttu-id="b660e-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b660e-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b660e-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b660e-148">-WhatIf</span></span>
<span data-ttu-id="b660e-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b660e-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b660e-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b660e-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b660e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b660e-151">CommonParameters</span></span>
<span data-ttu-id="b660e-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b660e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b660e-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b660e-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b660e-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b660e-154">INPUTS</span></span>

### <span data-ttu-id="b660e-155">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b660e-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b660e-156">System. String</span><span class="sxs-lookup"><span data-stu-id="b660e-156">System.String</span></span>

### <span data-ttu-id="b660e-157">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b660e-157">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b660e-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b660e-158">OUTPUTS</span></span>

### <span data-ttu-id="b660e-159">System. String</span><span class="sxs-lookup"><span data-stu-id="b660e-159">System.String</span></span>

## <span data-ttu-id="b660e-160">Note</span><span class="sxs-lookup"><span data-stu-id="b660e-160">NOTES</span></span>

## <span data-ttu-id="b660e-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b660e-161">RELATED LINKS</span></span>

[<span data-ttu-id="b660e-162">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b660e-162">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="b660e-163">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b660e-163">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


