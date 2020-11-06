---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: b5e51891f82b2a12f42fac3a1535f974912ca1dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515840"
---
# <span data-ttu-id="380ce-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="380ce-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="380ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="380ce-102">SYNOPSIS</span></span>
<span data-ttu-id="380ce-103">Aggiorna un backend.</span><span class="sxs-lookup"><span data-stu-id="380ce-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="380ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="380ce-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="380ce-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="380ce-105">DESCRIPTION</span></span>
<span data-ttu-id="380ce-106">Aggiorna un backend esistente nella gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="380ce-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="380ce-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="380ce-107">EXAMPLES</span></span>

### <span data-ttu-id="380ce-108">Aggiorna la descrizione del backend 123</span><span class="sxs-lookup"><span data-stu-id="380ce-108">Updates the Description of the Backend 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="380ce-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="380ce-109">PARAMETERS</span></span>

### <span data-ttu-id="380ce-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="380ce-110">-BackendId</span></span>
<span data-ttu-id="380ce-111">Identificatore del nuovo backend.</span><span class="sxs-lookup"><span data-stu-id="380ce-111">Identifier of new backend.</span></span>
<span data-ttu-id="380ce-112">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="380ce-112">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380ce-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="380ce-113">-Context</span></span>
<span data-ttu-id="380ce-114">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="380ce-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="380ce-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="380ce-115">This parameter is required.</span></span>

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

### <span data-ttu-id="380ce-116">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="380ce-116">-Credential</span></span>
<span data-ttu-id="380ce-117">Dettagli delle credenziali che dovrebbero essere usati per comunicare con il backend.</span><span class="sxs-lookup"><span data-stu-id="380ce-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="380ce-118">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="380ce-118">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementBackendCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380ce-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="380ce-119">-DefaultProfile</span></span>
<span data-ttu-id="380ce-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="380ce-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="380ce-121">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="380ce-121">-Description</span></span>
<span data-ttu-id="380ce-122">Descrizione del backend.</span><span class="sxs-lookup"><span data-stu-id="380ce-122">Backend Description.</span></span>
<span data-ttu-id="380ce-123">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="380ce-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="380ce-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="380ce-124">-PassThru</span></span>
<span data-ttu-id="380ce-125">Indica che questo cmdlet restituisce il  **PsApiManagementBackend** modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="380ce-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380ce-126">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="380ce-126">-Protocol</span></span>
<span data-ttu-id="380ce-127">Protocollo di comunicazione backend (http o SOAP).</span><span class="sxs-lookup"><span data-stu-id="380ce-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="380ce-128">Questo parametro è facoltativo</span><span class="sxs-lookup"><span data-stu-id="380ce-128">This parameter is optional</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380ce-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="380ce-129">-Proxy</span></span>
<span data-ttu-id="380ce-130">Dettagli del server proxy da usare durante l'invio di una richiesta al backend.</span><span class="sxs-lookup"><span data-stu-id="380ce-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="380ce-131">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="380ce-131">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380ce-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="380ce-132">-ResourceId</span></span>
<span data-ttu-id="380ce-133">URI di gestione della risorsa nel sistema esterno.</span><span class="sxs-lookup"><span data-stu-id="380ce-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="380ce-134">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="380ce-134">This parameter is optional.</span></span>
<span data-ttu-id="380ce-135">Questo URL può essere l'ID delle risorse ARM delle app logiche, delle app funzioni o delle app API.</span><span class="sxs-lookup"><span data-stu-id="380ce-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="380ce-136">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="380ce-136">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="380ce-137">Se ignorare la convalida della catena di certificati quando si parla con il backend.</span><span class="sxs-lookup"><span data-stu-id="380ce-137">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="380ce-138">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="380ce-138">This parameter is optional.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380ce-139">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="380ce-139">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="380ce-140">Se ignorare la convalida del nome del certificato quando si parla con il backend.</span><span class="sxs-lookup"><span data-stu-id="380ce-140">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="380ce-141">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="380ce-141">This parameter is optional.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380ce-142">-Titolo</span><span class="sxs-lookup"><span data-stu-id="380ce-142">-Title</span></span>
<span data-ttu-id="380ce-143">Titolo del backend.</span><span class="sxs-lookup"><span data-stu-id="380ce-143">Backend Title.</span></span>
<span data-ttu-id="380ce-144">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="380ce-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="380ce-145">-URL</span><span class="sxs-lookup"><span data-stu-id="380ce-145">-Url</span></span>
<span data-ttu-id="380ce-146">URL di runtime per il backend.</span><span class="sxs-lookup"><span data-stu-id="380ce-146">Runtime Url for the Backend.</span></span>
<span data-ttu-id="380ce-147">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="380ce-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="380ce-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="380ce-148">-Confirm</span></span>
<span data-ttu-id="380ce-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="380ce-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380ce-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="380ce-150">-WhatIf</span></span>
<span data-ttu-id="380ce-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="380ce-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="380ce-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="380ce-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380ce-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="380ce-153">CommonParameters</span></span>
<span data-ttu-id="380ce-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="380ce-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="380ce-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="380ce-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="380ce-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="380ce-156">INPUTS</span></span>

### <span data-ttu-id="380ce-157">Nessuno</span><span class="sxs-lookup"><span data-stu-id="380ce-157">None</span></span>
<span data-ttu-id="380ce-158">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="380ce-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="380ce-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="380ce-159">OUTPUTS</span></span>

### <span data-ttu-id="380ce-160">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="380ce-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="380ce-161">Note</span><span class="sxs-lookup"><span data-stu-id="380ce-161">NOTES</span></span>

## <span data-ttu-id="380ce-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="380ce-162">RELATED LINKS</span></span>

[<span data-ttu-id="380ce-163">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="380ce-163">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="380ce-164">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="380ce-164">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="380ce-165">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="380ce-165">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="380ce-166">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="380ce-166">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="380ce-167">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="380ce-167">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
