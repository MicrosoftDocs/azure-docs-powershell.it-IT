---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
ms.openlocfilehash: 3858d24bb0c714da0e48ad5834870ec5127eb5e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965342"
---
# <span data-ttu-id="a43e0-101">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a43e0-101">Set-AzApiManagementPolicy</span></span>

## <span data-ttu-id="a43e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a43e0-102">SYNOPSIS</span></span>
<span data-ttu-id="a43e0-103">Imposta il criterio di ambito specificato per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="a43e0-103">Sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="a43e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a43e0-104">SYNTAX</span></span>

### <span data-ttu-id="a43e0-105">SetTenantLevel (Default)</span><span class="sxs-lookup"><span data-stu-id="a43e0-105">SetTenantLevel (Default)</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a43e0-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="a43e0-106">SetProductLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a43e0-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="a43e0-107">SetApiLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a43e0-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="a43e0-108">SetOperationLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a43e0-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a43e0-109">DESCRIPTION</span></span>
<span data-ttu-id="a43e0-110">Il cmdlet **Set-AzApiManagementPolicy** imposta il criterio di ambito specificato per Gestione API.</span><span class="sxs-lookup"><span data-stu-id="a43e0-110">The **Set-AzApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="a43e0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a43e0-111">EXAMPLES</span></span>

### <span data-ttu-id="a43e0-112">Esempio 1: Impostare i criteri a livello di tenant</span><span class="sxs-lookup"><span data-stu-id="a43e0-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="a43e0-113">Questo comando imposta i criteri a livello di tenant da un file denominato tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="a43e0-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="a43e0-114">Esempio 2: Impostare un criterio di ambito del prodotto</span><span class="sxs-lookup"><span data-stu-id="a43e0-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="a43e0-115">Questo comando imposta i criteri di ambito del prodotto per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="a43e0-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="a43e0-116">Esempio 3: Impostare i criteri di ambito API</span><span class="sxs-lookup"><span data-stu-id="a43e0-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="a43e0-117">Questo comando imposta i criteri di ambito API per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="a43e0-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="a43e0-118">Esempio 4: Impostare i criteri di ambito delle operazioni</span><span class="sxs-lookup"><span data-stu-id="a43e0-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="a43e0-119">Questo comando imposta i criteri di ambito dell'operazione per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="a43e0-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="a43e0-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a43e0-120">PARAMETERS</span></span>

### <span data-ttu-id="a43e0-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a43e0-121">-ApiId</span></span>
<span data-ttu-id="a43e0-122">Specifica l'identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="a43e0-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="a43e0-123">Se si specifica questo parametro, il cmdlet imposta il criterio di ambito API.</span><span class="sxs-lookup"><span data-stu-id="a43e0-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

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

### <span data-ttu-id="a43e0-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="a43e0-124">-ApiRevision</span></span>
<span data-ttu-id="a43e0-125">Identificatore della revisione API.</span><span class="sxs-lookup"><span data-stu-id="a43e0-125">Identifier of API Revision.</span></span> <span data-ttu-id="a43e0-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a43e0-126">This parameter is optional.</span></span> <span data-ttu-id="a43e0-127">Se non viene specificato, il criterio verrà aggiornato nella revisione dell'API attualmente attiva.</span><span class="sxs-lookup"><span data-stu-id="a43e0-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="a43e0-128">-Context</span><span class="sxs-lookup"><span data-stu-id="a43e0-128">-Context</span></span>
<span data-ttu-id="a43e0-129">Specifica l'istanza di **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="a43e0-129">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="a43e0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a43e0-130">-DefaultProfile</span></span>
<span data-ttu-id="a43e0-131">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a43e0-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a43e0-132">-Format</span><span class="sxs-lookup"><span data-stu-id="a43e0-132">-Format</span></span>
<span data-ttu-id="a43e0-133">Specifica il formato del criterio.</span><span class="sxs-lookup"><span data-stu-id="a43e0-133">Specifies the format of the policy.</span></span> <span data-ttu-id="a43e0-134">Quando si usa `application/vnd.ms-azure-apim.policy+xml` , le espressioni contenute nel criterio devono usare il carattere di escape XML.</span><span class="sxs-lookup"><span data-stu-id="a43e0-134">When using `application/vnd.ms-azure-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="a43e0-135">Non è necessario usare il carattere di escape XML per `application/vnd.ms-azure-apim.policy.raw+xml` il criterio. </span><span class="sxs-lookup"><span data-stu-id="a43e0-135">When using `application/vnd.ms-azure-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="a43e0-136">Il valore predefinito è `application/vnd.ms-azure-apim.policy+xml` .</span><span class="sxs-lookup"><span data-stu-id="a43e0-136">The default value is `application/vnd.ms-azure-apim.policy+xml`.</span></span>
<span data-ttu-id="a43e0-137">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a43e0-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="a43e0-138">-OperationId</span><span class="sxs-lookup"><span data-stu-id="a43e0-138">-OperationId</span></span>
<span data-ttu-id="a43e0-139">Specifica l'identificatore dell'operazione esistente.</span><span class="sxs-lookup"><span data-stu-id="a43e0-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="a43e0-140">Se specificato con ApiId, imposta il criterio di ambito dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a43e0-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="a43e0-141">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="a43e0-141">This parameters is required.</span></span>

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

### <span data-ttu-id="a43e0-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a43e0-142">-PassThru</span></span>
<span data-ttu-id="a43e0-143">passthru</span><span class="sxs-lookup"><span data-stu-id="a43e0-143">passthru</span></span>

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

### <span data-ttu-id="a43e0-144">-Policy</span><span class="sxs-lookup"><span data-stu-id="a43e0-144">-Policy</span></span>
<span data-ttu-id="a43e0-145">Specifica il documento dei criteri come stringa.</span><span class="sxs-lookup"><span data-stu-id="a43e0-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="a43e0-146">Questo parametro è obbligatorio se non è specificato -*PolicyFilePath.*</span><span class="sxs-lookup"><span data-stu-id="a43e0-146">This parameter is required if the -*PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="a43e0-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="a43e0-147">-PolicyFilePath</span></span>
<span data-ttu-id="a43e0-148">Specifica il percorso del file di documento dei criteri.</span><span class="sxs-lookup"><span data-stu-id="a43e0-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="a43e0-149">Questo parametro è obbligatorio se *non è* specificato il parametro dei criteri.</span><span class="sxs-lookup"><span data-stu-id="a43e0-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="a43e0-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="a43e0-150">-PolicyUrl</span></span>
<span data-ttu-id="a43e0-151">URL in cui è ospitato il documento dei criteri.</span><span class="sxs-lookup"><span data-stu-id="a43e0-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="a43e0-152">Questo parametro è obbligatorio se non si specifica -Policy o -PolicyFilePath.</span><span class="sxs-lookup"><span data-stu-id="a43e0-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

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

### <span data-ttu-id="a43e0-153">-ProductId</span><span class="sxs-lookup"><span data-stu-id="a43e0-153">-ProductId</span></span>
<span data-ttu-id="a43e0-154">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="a43e0-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="a43e0-155">Se si specifica questo parametro, il cmdlet imposta i criteri di ambito del prodotto.</span><span class="sxs-lookup"><span data-stu-id="a43e0-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

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

### <span data-ttu-id="a43e0-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a43e0-156">CommonParameters</span></span>
<span data-ttu-id="a43e0-157">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a43e0-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a43e0-158">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a43e0-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a43e0-159">INPUT</span><span class="sxs-lookup"><span data-stu-id="a43e0-159">INPUTS</span></span>

### <span data-ttu-id="a43e0-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a43e0-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a43e0-161">System.String</span><span class="sxs-lookup"><span data-stu-id="a43e0-161">System.String</span></span>

### <span data-ttu-id="a43e0-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a43e0-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a43e0-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a43e0-163">OUTPUTS</span></span>

### <span data-ttu-id="a43e0-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a43e0-164">System.Boolean</span></span>

## <span data-ttu-id="a43e0-165">NOTE</span><span class="sxs-lookup"><span data-stu-id="a43e0-165">NOTES</span></span>

## <span data-ttu-id="a43e0-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a43e0-166">RELATED LINKS</span></span>

[<span data-ttu-id="a43e0-167">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a43e0-167">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="a43e0-168">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a43e0-168">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)


