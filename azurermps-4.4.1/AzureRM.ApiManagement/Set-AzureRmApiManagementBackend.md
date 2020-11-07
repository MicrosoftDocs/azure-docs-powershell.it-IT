---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: 85545777f5a76f3f75e81648a009ffcdcad8ab30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687741"
---
# <span data-ttu-id="bc034-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="bc034-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="bc034-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bc034-102">SYNOPSIS</span></span>
<span data-ttu-id="bc034-103">Aggiorna un backend.</span><span class="sxs-lookup"><span data-stu-id="bc034-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc034-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc034-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc034-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc034-105">DESCRIPTION</span></span>
<span data-ttu-id="bc034-106">Aggiorna un backend esistente nella gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="bc034-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="bc034-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc034-107">EXAMPLES</span></span>

### <span data-ttu-id="bc034-108">Aggiorna la descrizione del backend 123</span><span class="sxs-lookup"><span data-stu-id="bc034-108">Updates the Description of the Backend 123</span></span>
```
Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="bc034-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bc034-109">PARAMETERS</span></span>

### <span data-ttu-id="bc034-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="bc034-110">-BackendId</span></span>
<span data-ttu-id="bc034-111">Identificatore del nuovo backend.</span><span class="sxs-lookup"><span data-stu-id="bc034-111">Identifier of new backend.</span></span>
<span data-ttu-id="bc034-112">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="bc034-112">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc034-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="bc034-113">-Context</span></span>
<span data-ttu-id="bc034-114">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="bc034-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="bc034-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="bc034-115">This parameter is required.</span></span>

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

### <span data-ttu-id="bc034-116">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="bc034-116">-Credential</span></span>
<span data-ttu-id="bc034-117">Dettagli delle credenziali che dovrebbero essere usati per comunicare con il backend.</span><span class="sxs-lookup"><span data-stu-id="bc034-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="bc034-118">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bc034-118">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc034-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc034-119">-Description</span></span>
<span data-ttu-id="bc034-120">Descrizione del backend.</span><span class="sxs-lookup"><span data-stu-id="bc034-120">Backend Description.</span></span>
<span data-ttu-id="bc034-121">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bc034-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="bc034-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc034-122">-PassThru</span></span>
<span data-ttu-id="bc034-123">Indica che questo cmdlet restituisce il  **PsApiManagementBackend** modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc034-123">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc034-124">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="bc034-124">-Protocol</span></span>
<span data-ttu-id="bc034-125">Protocollo di comunicazione backend (http o SOAP).</span><span class="sxs-lookup"><span data-stu-id="bc034-125">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="bc034-126">Questo parametro è facoltativo</span><span class="sxs-lookup"><span data-stu-id="bc034-126">This parameter is optional</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc034-127">-Proxy</span><span class="sxs-lookup"><span data-stu-id="bc034-127">-Proxy</span></span>
<span data-ttu-id="bc034-128">Dettagli del server proxy da usare durante l'invio di una richiesta al backend.</span><span class="sxs-lookup"><span data-stu-id="bc034-128">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="bc034-129">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bc034-129">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc034-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc034-130">-ResourceId</span></span>
<span data-ttu-id="bc034-131">URI di gestione della risorsa nel sistema esterno.</span><span class="sxs-lookup"><span data-stu-id="bc034-131">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="bc034-132">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bc034-132">This parameter is optional.</span></span>
<span data-ttu-id="bc034-133">Questo URL può essere l'ID delle risorse ARM delle app logiche, delle app funzioni o delle app API.</span><span class="sxs-lookup"><span data-stu-id="bc034-133">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="bc034-134">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="bc034-134">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="bc034-135">Se ignorare la convalida della catena di certificati quando si parla con il backend.</span><span class="sxs-lookup"><span data-stu-id="bc034-135">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="bc034-136">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bc034-136">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc034-137">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="bc034-137">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="bc034-138">Se ignorare la convalida del nome del certificato quando si parla con il backend.</span><span class="sxs-lookup"><span data-stu-id="bc034-138">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="bc034-139">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bc034-139">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc034-140">-Titolo</span><span class="sxs-lookup"><span data-stu-id="bc034-140">-Title</span></span>
<span data-ttu-id="bc034-141">Titolo del backend.</span><span class="sxs-lookup"><span data-stu-id="bc034-141">Backend Title.</span></span>
<span data-ttu-id="bc034-142">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bc034-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="bc034-143">-URL</span><span class="sxs-lookup"><span data-stu-id="bc034-143">-Url</span></span>
<span data-ttu-id="bc034-144">URL di runtime per il backend.</span><span class="sxs-lookup"><span data-stu-id="bc034-144">Runtime Url for the Backend.</span></span>
<span data-ttu-id="bc034-145">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bc034-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="bc034-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bc034-146">-Confirm</span></span>
<span data-ttu-id="bc034-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc034-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc034-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc034-148">-WhatIf</span></span>
<span data-ttu-id="bc034-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc034-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc034-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc034-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc034-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc034-151">-DefaultProfile</span></span>
<span data-ttu-id="bc034-152">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc034-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc034-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc034-153">CommonParameters</span></span>
<span data-ttu-id="bc034-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc034-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc034-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc034-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc034-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bc034-156">INPUTS</span></span>

## <span data-ttu-id="bc034-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc034-157">OUTPUTS</span></span>

### <span data-ttu-id="bc034-158">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="bc034-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="bc034-159">Note</span><span class="sxs-lookup"><span data-stu-id="bc034-159">NOTES</span></span>

## <span data-ttu-id="bc034-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc034-160">RELATED LINKS</span></span>

[<span data-ttu-id="bc034-161">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="bc034-161">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="bc034-162">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="bc034-162">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="bc034-163">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="bc034-163">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="bc034-164">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="bc034-164">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="bc034-165">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="bc034-165">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
