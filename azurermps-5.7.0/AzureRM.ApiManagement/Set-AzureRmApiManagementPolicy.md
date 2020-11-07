---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 0f9ee1c2190dbc3d657ecc52cd85b6af8b0cac4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686122"
---
# <span data-ttu-id="ceb1f-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ceb1f-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="ceb1f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ceb1f-102">SYNOPSIS</span></span>
<span data-ttu-id="ceb1f-103">Imposta il criterio di ambito specificato per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ceb1f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ceb1f-104">SYNTAX</span></span>

### <span data-ttu-id="ceb1f-105">SetTenantLevel (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ceb1f-105">SetTenantLevel (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ceb1f-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="ceb1f-106">SetProductLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ceb1f-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="ceb1f-107">SetApiLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ceb1f-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="ceb1f-108">SetOperationLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ceb1f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ceb1f-109">DESCRIPTION</span></span>
<span data-ttu-id="ceb1f-110">Il cmdlet **set-AzureRmApiManagementPolicy** imposta i criteri di ambito specificati per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="ceb1f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ceb1f-111">EXAMPLES</span></span>

### <span data-ttu-id="ceb1f-112">Esempio 1: impostare i criteri di livello tenant</span><span class="sxs-lookup"><span data-stu-id="ceb1f-112">Example 1: Set the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="ceb1f-113">Questo comando imposta i criteri del livello del tenant da un file denominato tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="ceb1f-114">Esempio 2: impostare un criterio per l'ambito prodotto</span><span class="sxs-lookup"><span data-stu-id="ceb1f-114">Example 2: Set a product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="ceb1f-115">Questo comando imposta il criterio dell'ambito dei prodotti per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="ceb1f-116">Esempio 3: impostare i criteri per l'ambito API</span><span class="sxs-lookup"><span data-stu-id="ceb1f-116">Example 3: Set API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="ceb1f-117">Questo comando imposta i criteri per l'ambito API per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="ceb1f-118">Esempio 4: impostare i criteri per l'ambito delle operazioni</span><span class="sxs-lookup"><span data-stu-id="ceb1f-118">Example 4: Set operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="ceb1f-119">Questo comando imposta i criteri per l'ambito dell'operazione per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="ceb1f-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ceb1f-120">PARAMETERS</span></span>

### <span data-ttu-id="ceb1f-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ceb1f-121">-ApiId</span></span>
<span data-ttu-id="ceb1f-122">Specifica l'identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="ceb1f-123">Se specifichi questo parametro, il cmdlet imposta i criteri per l'ambito API.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceb1f-124">-Contesto</span><span class="sxs-lookup"><span data-stu-id="ceb1f-124">-Context</span></span>
<span data-ttu-id="ceb1f-125">Specifica l'istanza di **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-125">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="ceb1f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceb1f-126">-DefaultProfile</span></span>
<span data-ttu-id="ceb1f-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="ceb1f-128">-Format</span><span class="sxs-lookup"><span data-stu-id="ceb1f-128">-Format</span></span>
<span data-ttu-id="ceb1f-129">Specifica il formato del criterio.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-129">Specifies the format of the policy.</span></span>
<span data-ttu-id="ceb1f-130">Il valore predefinito è "application/vnd. ms-Azure-APIM. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="ceb1f-130">The default value is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="ceb1f-131">-OperationId</span><span class="sxs-lookup"><span data-stu-id="ceb1f-131">-OperationId</span></span>
<span data-ttu-id="ceb1f-132">Specifica l'identificatore dell'operazione esistente.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-132">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="ceb1f-133">Se specificato con ApiId imposterà i criteri per l'ambito delle operazioni.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-133">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="ceb1f-134">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-134">This parameters is required.</span></span>

```yaml
Type: String
Parameter Sets: SetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceb1f-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ceb1f-135">-PassThru</span></span>
<span data-ttu-id="ceb1f-136">PassThru</span><span class="sxs-lookup"><span data-stu-id="ceb1f-136">passthru</span></span>

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

### <span data-ttu-id="ceb1f-137">-Policy</span><span class="sxs-lookup"><span data-stu-id="ceb1f-137">-Policy</span></span>
<span data-ttu-id="ceb1f-138">Specifica il documento di criteri come stringa.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-138">Specifies the policy document as a string.</span></span>
<span data-ttu-id="ceb1f-139">Questo parametro è obbligatorio se non è specificato- *PolicyFilePath* .</span><span class="sxs-lookup"><span data-stu-id="ceb1f-139">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="ceb1f-140">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="ceb1f-140">-PolicyFilePath</span></span>
<span data-ttu-id="ceb1f-141">Specifica il percorso del file del documento dei criteri.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-141">Specifies the policy document file path.</span></span>
<span data-ttu-id="ceb1f-142">Questo parametro è obbligatorio se il parametro *policy* non è specificato.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-142">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="ceb1f-143">-ProductId</span><span class="sxs-lookup"><span data-stu-id="ceb1f-143">-ProductId</span></span>
<span data-ttu-id="ceb1f-144">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-144">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="ceb1f-145">Se questo parametro viene specificato, il cmdlet imposta il criterio dell'ambito del prodotto.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-145">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: SetProductLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceb1f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceb1f-146">CommonParameters</span></span>
<span data-ttu-id="ceb1f-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceb1f-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceb1f-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceb1f-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ceb1f-149">INPUTS</span></span>

### <span data-ttu-id="ceb1f-150">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ceb1f-150">None</span></span>
<span data-ttu-id="ceb1f-151">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ceb1f-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ceb1f-152">OUTPUTS</span></span>

### <span data-ttu-id="ceb1f-153">bool</span><span class="sxs-lookup"><span data-stu-id="ceb1f-153">bool</span></span>

## <span data-ttu-id="ceb1f-154">Note</span><span class="sxs-lookup"><span data-stu-id="ceb1f-154">NOTES</span></span>

## <span data-ttu-id="ceb1f-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ceb1f-155">RELATED LINKS</span></span>

[<span data-ttu-id="ceb1f-156">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ceb1f-156">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="ceb1f-157">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ceb1f-157">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


