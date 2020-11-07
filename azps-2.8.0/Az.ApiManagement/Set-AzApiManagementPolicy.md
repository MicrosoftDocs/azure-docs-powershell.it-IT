---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
ms.openlocfilehash: 7398687bed785b0152b991656baf2784df204ed6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675885"
---
# <span data-ttu-id="f8a63-101">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f8a63-101">Set-AzApiManagementPolicy</span></span>

## <span data-ttu-id="f8a63-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8a63-102">SYNOPSIS</span></span>
<span data-ttu-id="f8a63-103">Imposta il criterio di ambito specificato per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="f8a63-103">Sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="f8a63-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8a63-104">SYNTAX</span></span>

### <span data-ttu-id="f8a63-105">SetTenantLevel (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f8a63-105">SetTenantLevel (Default)</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8a63-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="f8a63-106">SetProductLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8a63-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="f8a63-107">SetApiLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8a63-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="f8a63-108">SetOperationLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8a63-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8a63-109">DESCRIPTION</span></span>
<span data-ttu-id="f8a63-110">Il cmdlet **set-AzApiManagementPolicy** imposta i criteri di ambito specificati per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="f8a63-110">The **Set-AzApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="f8a63-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8a63-111">EXAMPLES</span></span>

### <span data-ttu-id="f8a63-112">Esempio 1: impostare i criteri di livello tenant</span><span class="sxs-lookup"><span data-stu-id="f8a63-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="f8a63-113">Questo comando imposta i criteri del livello del tenant da un file denominato tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="f8a63-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="f8a63-114">Esempio 2: impostare un criterio per l'ambito prodotto</span><span class="sxs-lookup"><span data-stu-id="f8a63-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="f8a63-115">Questo comando imposta il criterio dell'ambito dei prodotti per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="f8a63-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="f8a63-116">Esempio 3: impostare i criteri per l'ambito API</span><span class="sxs-lookup"><span data-stu-id="f8a63-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="f8a63-117">Questo comando imposta i criteri per l'ambito API per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="f8a63-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="f8a63-118">Esempio 4: impostare i criteri per l'ambito delle operazioni</span><span class="sxs-lookup"><span data-stu-id="f8a63-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="f8a63-119">Questo comando imposta i criteri per l'ambito dell'operazione per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="f8a63-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="f8a63-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8a63-120">PARAMETERS</span></span>

### <span data-ttu-id="f8a63-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f8a63-121">-ApiId</span></span>
<span data-ttu-id="f8a63-122">Specifica l'identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="f8a63-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="f8a63-123">Se specifichi questo parametro, il cmdlet imposta i criteri per l'ambito API.</span><span class="sxs-lookup"><span data-stu-id="f8a63-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

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

### <span data-ttu-id="f8a63-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="f8a63-124">-ApiRevision</span></span>
<span data-ttu-id="f8a63-125">Identificatore della revisione API.</span><span class="sxs-lookup"><span data-stu-id="f8a63-125">Identifier of API Revision.</span></span> <span data-ttu-id="f8a63-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f8a63-126">This parameter is optional.</span></span> <span data-ttu-id="f8a63-127">Se non specificato, il criterio verrà aggiornato nella revisione API attualmente attiva.</span><span class="sxs-lookup"><span data-stu-id="f8a63-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="f8a63-128">-Contesto</span><span class="sxs-lookup"><span data-stu-id="f8a63-128">-Context</span></span>
<span data-ttu-id="f8a63-129">Specifica l'istanza di **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="f8a63-129">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="f8a63-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8a63-130">-DefaultProfile</span></span>
<span data-ttu-id="f8a63-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f8a63-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8a63-132">-Format</span><span class="sxs-lookup"><span data-stu-id="f8a63-132">-Format</span></span>
<span data-ttu-id="f8a63-133">Specifica il formato del criterio.</span><span class="sxs-lookup"><span data-stu-id="f8a63-133">Specifies the format of the policy.</span></span> <span data-ttu-id="f8a63-134">Quando `application/vnd.ms-azure-apim.policy+xml` si usa, le espressioni contenute nel criterio devono essere di escape XML.</span><span class="sxs-lookup"><span data-stu-id="f8a63-134">When using `application/vnd.ms-azure-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="f8a63-135">Quando si usa `application/vnd.ms-azure-apim.policy.raw+xml` **non** è necessario che il criterio sia di escape XML.</span><span class="sxs-lookup"><span data-stu-id="f8a63-135">When using `application/vnd.ms-azure-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="f8a63-136">Il valore predefinito è `application/vnd.ms-azure-apim.policy+xml` .</span><span class="sxs-lookup"><span data-stu-id="f8a63-136">The default value is `application/vnd.ms-azure-apim.policy+xml`.</span></span>
<span data-ttu-id="f8a63-137">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f8a63-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="f8a63-138">-OperationId</span><span class="sxs-lookup"><span data-stu-id="f8a63-138">-OperationId</span></span>
<span data-ttu-id="f8a63-139">Specifica l'identificatore dell'operazione esistente.</span><span class="sxs-lookup"><span data-stu-id="f8a63-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="f8a63-140">Se specificato con ApiId imposterà i criteri per l'ambito delle operazioni.</span><span class="sxs-lookup"><span data-stu-id="f8a63-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="f8a63-141">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f8a63-141">This parameters is required.</span></span>

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

### <span data-ttu-id="f8a63-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8a63-142">-PassThru</span></span>
<span data-ttu-id="f8a63-143">PassThru</span><span class="sxs-lookup"><span data-stu-id="f8a63-143">passthru</span></span>

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

### <span data-ttu-id="f8a63-144">-Policy</span><span class="sxs-lookup"><span data-stu-id="f8a63-144">-Policy</span></span>
<span data-ttu-id="f8a63-145">Specifica il documento di criteri come stringa.</span><span class="sxs-lookup"><span data-stu-id="f8a63-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="f8a63-146">Questo parametro è obbligatorio se non è specificato- *PolicyFilePath* .</span><span class="sxs-lookup"><span data-stu-id="f8a63-146">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="f8a63-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="f8a63-147">-PolicyFilePath</span></span>
<span data-ttu-id="f8a63-148">Specifica il percorso del file del documento dei criteri.</span><span class="sxs-lookup"><span data-stu-id="f8a63-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="f8a63-149">Questo parametro è obbligatorio se il parametro *policy* non è specificato.</span><span class="sxs-lookup"><span data-stu-id="f8a63-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="f8a63-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="f8a63-150">-PolicyUrl</span></span>
<span data-ttu-id="f8a63-151">URL in cui è ospitato il documento dei criteri.</span><span class="sxs-lookup"><span data-stu-id="f8a63-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="f8a63-152">Questo parametro è obbligatorio se-Policy o-PolicyFilePath non è specificato.</span><span class="sxs-lookup"><span data-stu-id="f8a63-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

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

### <span data-ttu-id="f8a63-153">-ProductId</span><span class="sxs-lookup"><span data-stu-id="f8a63-153">-ProductId</span></span>
<span data-ttu-id="f8a63-154">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="f8a63-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="f8a63-155">Se questo parametro viene specificato, il cmdlet imposta il criterio dell'ambito del prodotto.</span><span class="sxs-lookup"><span data-stu-id="f8a63-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

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

### <span data-ttu-id="f8a63-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8a63-156">CommonParameters</span></span>
<span data-ttu-id="f8a63-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8a63-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8a63-158">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8a63-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8a63-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8a63-159">INPUTS</span></span>

### <span data-ttu-id="f8a63-160">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f8a63-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f8a63-161">System. String</span><span class="sxs-lookup"><span data-stu-id="f8a63-161">System.String</span></span>

### <span data-ttu-id="f8a63-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f8a63-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f8a63-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8a63-163">OUTPUTS</span></span>

### <span data-ttu-id="f8a63-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f8a63-164">System.Boolean</span></span>

## <span data-ttu-id="f8a63-165">Note</span><span class="sxs-lookup"><span data-stu-id="f8a63-165">NOTES</span></span>

## <span data-ttu-id="f8a63-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8a63-166">RELATED LINKS</span></span>

[<span data-ttu-id="f8a63-167">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f8a63-167">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="f8a63-168">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f8a63-168">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)


