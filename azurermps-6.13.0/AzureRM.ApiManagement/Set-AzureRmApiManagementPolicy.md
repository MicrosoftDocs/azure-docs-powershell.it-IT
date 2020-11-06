---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 75bb963195244a5a1a27ca004eb2795b6b5bb556
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509427"
---
# <span data-ttu-id="25d08-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="25d08-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="25d08-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="25d08-102">SYNOPSIS</span></span>
<span data-ttu-id="25d08-103">Imposta il criterio di ambito specificato per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="25d08-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25d08-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="25d08-104">SYNTAX</span></span>

### <span data-ttu-id="25d08-105">SetTenantLevel (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="25d08-105">SetTenantLevel (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25d08-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="25d08-106">SetProductLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25d08-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="25d08-107">SetApiLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25d08-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="25d08-108">SetOperationLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25d08-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25d08-109">DESCRIPTION</span></span>
<span data-ttu-id="25d08-110">Il cmdlet **set-AzureRmApiManagementPolicy** imposta i criteri di ambito specificati per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="25d08-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="25d08-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="25d08-111">EXAMPLES</span></span>

### <span data-ttu-id="25d08-112">Esempio 1: impostare i criteri di livello tenant</span><span class="sxs-lookup"><span data-stu-id="25d08-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="25d08-113">Questo comando imposta i criteri del livello del tenant da un file denominato tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="25d08-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="25d08-114">Esempio 2: impostare un criterio per l'ambito prodotto</span><span class="sxs-lookup"><span data-stu-id="25d08-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="25d08-115">Questo comando imposta il criterio dell'ambito dei prodotti per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="25d08-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="25d08-116">Esempio 3: impostare i criteri per l'ambito API</span><span class="sxs-lookup"><span data-stu-id="25d08-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="25d08-117">Questo comando imposta i criteri per l'ambito API per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="25d08-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="25d08-118">Esempio 4: impostare i criteri per l'ambito delle operazioni</span><span class="sxs-lookup"><span data-stu-id="25d08-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="25d08-119">Questo comando imposta i criteri per l'ambito dell'operazione per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="25d08-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="25d08-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="25d08-120">PARAMETERS</span></span>

### <span data-ttu-id="25d08-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="25d08-121">-ApiId</span></span>
<span data-ttu-id="25d08-122">Specifica l'identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="25d08-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="25d08-123">Se specifichi questo parametro, il cmdlet imposta i criteri per l'ambito API.</span><span class="sxs-lookup"><span data-stu-id="25d08-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d08-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="25d08-124">-ApiRevision</span></span>
<span data-ttu-id="25d08-125">Identificatore della revisione API.</span><span class="sxs-lookup"><span data-stu-id="25d08-125">Identifier of API Revision.</span></span> <span data-ttu-id="25d08-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="25d08-126">This parameter is optional.</span></span> <span data-ttu-id="25d08-127">Se non specificato, il criterio verrà aggiornato nella revisione API attualmente attiva.</span><span class="sxs-lookup"><span data-stu-id="25d08-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d08-128">-Contesto</span><span class="sxs-lookup"><span data-stu-id="25d08-128">-Context</span></span>
<span data-ttu-id="25d08-129">Specifica l'istanza di **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="25d08-129">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="25d08-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25d08-130">-DefaultProfile</span></span>
<span data-ttu-id="25d08-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="25d08-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25d08-132">-Format</span><span class="sxs-lookup"><span data-stu-id="25d08-132">-Format</span></span>
<span data-ttu-id="25d08-133">Specifica il formato del criterio.</span><span class="sxs-lookup"><span data-stu-id="25d08-133">Specifies the format of the policy.</span></span> <span data-ttu-id="25d08-134">Quando `application/vnd.ms-azure-apim.policy+xml` si usa, le espressioni contenute nel criterio devono essere di escape XML.</span><span class="sxs-lookup"><span data-stu-id="25d08-134">When using `application/vnd.ms-azure-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="25d08-135">Quando si usa `application/vnd.ms-azure-apim.policy.raw+xml` **non** è necessario che il criterio sia di escape XML.</span><span class="sxs-lookup"><span data-stu-id="25d08-135">When using `application/vnd.ms-azure-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="25d08-136">Il valore predefinito è `application/vnd.ms-azure-apim.policy+xml` .</span><span class="sxs-lookup"><span data-stu-id="25d08-136">The default value is `application/vnd.ms-azure-apim.policy+xml`.</span></span>
<span data-ttu-id="25d08-137">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="25d08-137">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: application/vnd.ms-azure-apim.policy.raw+xml, application/vnd.ms-azure-apim.policy+xml

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d08-138">-OperationId</span><span class="sxs-lookup"><span data-stu-id="25d08-138">-OperationId</span></span>
<span data-ttu-id="25d08-139">Specifica l'identificatore dell'operazione esistente.</span><span class="sxs-lookup"><span data-stu-id="25d08-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="25d08-140">Se specificato con ApiId imposterà i criteri per l'ambito delle operazioni.</span><span class="sxs-lookup"><span data-stu-id="25d08-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="25d08-141">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="25d08-141">This parameters is required.</span></span>

```yaml
Type: System.String
Parameter Sets: SetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d08-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25d08-142">-PassThru</span></span>
<span data-ttu-id="25d08-143">PassThru</span><span class="sxs-lookup"><span data-stu-id="25d08-143">passthru</span></span>

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

### <span data-ttu-id="25d08-144">-Policy</span><span class="sxs-lookup"><span data-stu-id="25d08-144">-Policy</span></span>
<span data-ttu-id="25d08-145">Specifica il documento di criteri come stringa.</span><span class="sxs-lookup"><span data-stu-id="25d08-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="25d08-146">Questo parametro è obbligatorio se non è specificato- *PolicyFilePath* .</span><span class="sxs-lookup"><span data-stu-id="25d08-146">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="25d08-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="25d08-147">-PolicyFilePath</span></span>
<span data-ttu-id="25d08-148">Specifica il percorso del file del documento dei criteri.</span><span class="sxs-lookup"><span data-stu-id="25d08-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="25d08-149">Questo parametro è obbligatorio se il parametro *policy* non è specificato.</span><span class="sxs-lookup"><span data-stu-id="25d08-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="25d08-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="25d08-150">-PolicyUrl</span></span>
<span data-ttu-id="25d08-151">URL in cui è ospitato il documento dei criteri.</span><span class="sxs-lookup"><span data-stu-id="25d08-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="25d08-152">Questo parametro è obbligatorio se-Policy o-PolicyFilePath non è specificato.</span><span class="sxs-lookup"><span data-stu-id="25d08-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

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

### <span data-ttu-id="25d08-153">-ProductId</span><span class="sxs-lookup"><span data-stu-id="25d08-153">-ProductId</span></span>
<span data-ttu-id="25d08-154">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="25d08-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="25d08-155">Se questo parametro viene specificato, il cmdlet imposta il criterio dell'ambito del prodotto.</span><span class="sxs-lookup"><span data-stu-id="25d08-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d08-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d08-156">CommonParameters</span></span>
<span data-ttu-id="25d08-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25d08-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d08-158">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25d08-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d08-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="25d08-159">INPUTS</span></span>

### <span data-ttu-id="25d08-160">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="25d08-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="25d08-161">System. String</span><span class="sxs-lookup"><span data-stu-id="25d08-161">System.String</span></span>

### <span data-ttu-id="25d08-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="25d08-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="25d08-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="25d08-163">OUTPUTS</span></span>

### <span data-ttu-id="25d08-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25d08-164">System.Boolean</span></span>

## <span data-ttu-id="25d08-165">Note</span><span class="sxs-lookup"><span data-stu-id="25d08-165">NOTES</span></span>

## <span data-ttu-id="25d08-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="25d08-166">RELATED LINKS</span></span>

[<span data-ttu-id="25d08-167">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="25d08-167">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="25d08-168">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="25d08-168">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


