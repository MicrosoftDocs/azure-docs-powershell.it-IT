---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 8073df3946f5bf42ee8b0e5f2c7ae7881e905eaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517172"
---
# <span data-ttu-id="48053-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="48053-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="48053-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="48053-102">SYNOPSIS</span></span>
<span data-ttu-id="48053-103">Imposta il criterio di ambito specificato per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="48053-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48053-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48053-104">SYNTAX</span></span>

### <span data-ttu-id="48053-105">Livello tenant (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="48053-105">Tenant level (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48053-106">Livello di prodotto</span><span class="sxs-lookup"><span data-stu-id="48053-106">Product level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="48053-107">Livello API</span><span class="sxs-lookup"><span data-stu-id="48053-107">API level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="48053-108">Livello di operazione</span><span class="sxs-lookup"><span data-stu-id="48053-108">Operation level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48053-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48053-109">DESCRIPTION</span></span>
<span data-ttu-id="48053-110">Il cmdlet **set-AzureRmApiManagementPolicy** imposta i criteri di ambito specificati per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="48053-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="48053-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48053-111">EXAMPLES</span></span>

### <span data-ttu-id="48053-112">Esempio 1: impostare i criteri di livello tenant</span><span class="sxs-lookup"><span data-stu-id="48053-112">Example 1: Set the tenant level policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="48053-113">Questo comando imposta i criteri del livello del tenant da un file denominato tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="48053-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="48053-114">Esempio 2: impostare un criterio per l'ambito prodotto</span><span class="sxs-lookup"><span data-stu-id="48053-114">Example 2: Set a product-scope policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="48053-115">Questo comando imposta il criterio dell'ambito dei prodotti per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="48053-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="48053-116">Esempio 3: impostare i criteri per l'ambito API</span><span class="sxs-lookup"><span data-stu-id="48053-116">Example 3: Set API-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="48053-117">Questo comando imposta i criteri per l'ambito API per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="48053-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="48053-118">Esempio 4: impostare i criteri per l'ambito delle operazioni</span><span class="sxs-lookup"><span data-stu-id="48053-118">Example 4: Set operation-scope policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="48053-119">Questo comando imposta i criteri per l'ambito dell'operazione per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="48053-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="48053-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="48053-120">PARAMETERS</span></span>

### <span data-ttu-id="48053-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="48053-121">-ApiId</span></span>
<span data-ttu-id="48053-122">Specifica l'identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="48053-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="48053-123">Se specifichi questo parametro, il cmdlet imposta i criteri per l'ambito API.</span><span class="sxs-lookup"><span data-stu-id="48053-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

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

### <span data-ttu-id="48053-124">-Contesto</span><span class="sxs-lookup"><span data-stu-id="48053-124">-Context</span></span>
<span data-ttu-id="48053-125">Specifica l'istanza di **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="48053-125">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="48053-126">-Format</span><span class="sxs-lookup"><span data-stu-id="48053-126">-Format</span></span>
<span data-ttu-id="48053-127">Specifica il formato del criterio.</span><span class="sxs-lookup"><span data-stu-id="48053-127">Specifies the format of the policy.</span></span>
<span data-ttu-id="48053-128">Il valore predefinito è "application/vnd. ms-Azure-APIM. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="48053-128">The default value is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="48053-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="48053-129">-OperationId</span></span>
<span data-ttu-id="48053-130">Specifica l'identificatore dell'operazione esistente.</span><span class="sxs-lookup"><span data-stu-id="48053-130">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="48053-131">Se specificato con ApiId imposterà i criteri per l'ambito delle operazioni.</span><span class="sxs-lookup"><span data-stu-id="48053-131">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="48053-132">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="48053-132">This parameters is required.</span></span>

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

### <span data-ttu-id="48053-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48053-133">-PassThru</span></span>
<span data-ttu-id="48053-134">PassThru</span><span class="sxs-lookup"><span data-stu-id="48053-134">passthru</span></span>

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

### <span data-ttu-id="48053-135">-Policy</span><span class="sxs-lookup"><span data-stu-id="48053-135">-Policy</span></span>
<span data-ttu-id="48053-136">Specifica il documento di criteri come stringa.</span><span class="sxs-lookup"><span data-stu-id="48053-136">Specifies the policy document as a string.</span></span>
<span data-ttu-id="48053-137">Questo parametro è obbligatorio se non è specificato- *PolicyFilePath* .</span><span class="sxs-lookup"><span data-stu-id="48053-137">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="48053-138">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="48053-138">-PolicyFilePath</span></span>
<span data-ttu-id="48053-139">Specifica il percorso del file del documento dei criteri.</span><span class="sxs-lookup"><span data-stu-id="48053-139">Specifies the policy document file path.</span></span>
<span data-ttu-id="48053-140">Questo parametro è obbligatorio se il parametro *policy* non è specificato.</span><span class="sxs-lookup"><span data-stu-id="48053-140">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="48053-141">-ProductId</span><span class="sxs-lookup"><span data-stu-id="48053-141">-ProductId</span></span>
<span data-ttu-id="48053-142">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="48053-142">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="48053-143">Se questo parametro viene specificato, il cmdlet imposta il criterio dell'ambito del prodotto.</span><span class="sxs-lookup"><span data-stu-id="48053-143">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

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

### <span data-ttu-id="48053-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48053-144">-DefaultProfile</span></span>
<span data-ttu-id="48053-145">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="48053-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48053-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48053-146">CommonParameters</span></span>
<span data-ttu-id="48053-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48053-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48053-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48053-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48053-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="48053-149">INPUTS</span></span>

## <span data-ttu-id="48053-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48053-150">OUTPUTS</span></span>

### <span data-ttu-id="48053-151">bool</span><span class="sxs-lookup"><span data-stu-id="48053-151">bool</span></span>

## <span data-ttu-id="48053-152">Note</span><span class="sxs-lookup"><span data-stu-id="48053-152">NOTES</span></span>

## <span data-ttu-id="48053-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48053-153">RELATED LINKS</span></span>

[<span data-ttu-id="48053-154">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="48053-154">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="48053-155">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="48053-155">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


