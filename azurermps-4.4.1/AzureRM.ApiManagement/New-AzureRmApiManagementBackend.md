---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: 144830c2155379683c8568eda6e0d1bc021b38fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517232"
---
# <span data-ttu-id="fca70-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fca70-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="fca70-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fca70-102">SYNOPSIS</span></span>
<span data-ttu-id="fca70-103">Crea una nuova entità back-end.</span><span class="sxs-lookup"><span data-stu-id="fca70-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fca70-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fca70-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fca70-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fca70-105">DESCRIPTION</span></span>
<span data-ttu-id="fca70-106">Crea una nuova entità back-end nella gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="fca70-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="fca70-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fca70-107">EXAMPLES</span></span>

### <span data-ttu-id="fca70-108">Creare un backend 123 con uno schema di autorizzazione di base</span><span class="sxs-lookup"><span data-stu-id="fca70-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```
$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="fca70-109">Crea un nuovo backend</span><span class="sxs-lookup"><span data-stu-id="fca70-109">Creates a new Backend</span></span>

## <span data-ttu-id="fca70-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fca70-110">PARAMETERS</span></span>

### <span data-ttu-id="fca70-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="fca70-111">-BackendId</span></span>
<span data-ttu-id="fca70-112">Identificatore del nuovo backend.</span><span class="sxs-lookup"><span data-stu-id="fca70-112">Identifier of new backend.</span></span>
<span data-ttu-id="fca70-113">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fca70-113">This parameter is optional.</span></span>
<span data-ttu-id="fca70-114">Se non viene specificato verrà generato.</span><span class="sxs-lookup"><span data-stu-id="fca70-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="fca70-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="fca70-115">-Context</span></span>
<span data-ttu-id="fca70-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="fca70-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fca70-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="fca70-117">This parameter is required.</span></span>

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

### <span data-ttu-id="fca70-118">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="fca70-118">-Credential</span></span>
<span data-ttu-id="fca70-119">Dettagli delle credenziali che dovrebbero essere usati per comunicare con il backend.</span><span class="sxs-lookup"><span data-stu-id="fca70-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="fca70-120">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fca70-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="fca70-121">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="fca70-121">-Description</span></span>
<span data-ttu-id="fca70-122">Descrizione del backend.</span><span class="sxs-lookup"><span data-stu-id="fca70-122">Backend Description.</span></span>
<span data-ttu-id="fca70-123">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fca70-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="fca70-124">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="fca70-124">-Protocol</span></span>
<span data-ttu-id="fca70-125">Protocollo di comunicazione backend.</span><span class="sxs-lookup"><span data-stu-id="fca70-125">Backend Communication protocol.</span></span>
<span data-ttu-id="fca70-126">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="fca70-126">This parameter is required.</span></span>
<span data-ttu-id="fca70-127">I valori validi sono "http" e "SOAP".</span><span class="sxs-lookup"><span data-stu-id="fca70-127">Valid values are 'http' and 'soap'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fca70-128">-Proxy</span><span class="sxs-lookup"><span data-stu-id="fca70-128">-Proxy</span></span>
<span data-ttu-id="fca70-129">Dettagli del server proxy da usare durante l'invio di una richiesta al backend.</span><span class="sxs-lookup"><span data-stu-id="fca70-129">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="fca70-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fca70-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="fca70-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fca70-131">-ResourceId</span></span>
<span data-ttu-id="fca70-132">URI di gestione della risorsa nel sistema esterno.</span><span class="sxs-lookup"><span data-stu-id="fca70-132">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="fca70-133">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fca70-133">This parameter is optional.</span></span>
<span data-ttu-id="fca70-134">Questo URL può essere l'ID delle risorse ARM delle app logiche, delle app funzioni o delle app API.</span><span class="sxs-lookup"><span data-stu-id="fca70-134">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="fca70-135">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="fca70-135">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="fca70-136">Se ignorare la convalida della catena di certificati quando si parla con il backend.</span><span class="sxs-lookup"><span data-stu-id="fca70-136">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="fca70-137">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fca70-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="fca70-138">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="fca70-138">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="fca70-139">Se ignorare la convalida del nome del certificato quando si parla con il backend.</span><span class="sxs-lookup"><span data-stu-id="fca70-139">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="fca70-140">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fca70-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="fca70-141">-Titolo</span><span class="sxs-lookup"><span data-stu-id="fca70-141">-Title</span></span>
<span data-ttu-id="fca70-142">Titolo del backend.</span><span class="sxs-lookup"><span data-stu-id="fca70-142">Backend Title.</span></span>
<span data-ttu-id="fca70-143">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fca70-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="fca70-144">-URL</span><span class="sxs-lookup"><span data-stu-id="fca70-144">-Url</span></span>
<span data-ttu-id="fca70-145">URL di runtime per il backend.</span><span class="sxs-lookup"><span data-stu-id="fca70-145">Runtime Url for the Backend.</span></span>
<span data-ttu-id="fca70-146">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="fca70-146">This parameter is required.</span></span>

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

### <span data-ttu-id="fca70-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fca70-147">-Confirm</span></span>
<span data-ttu-id="fca70-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fca70-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fca70-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fca70-149">-WhatIf</span></span>
<span data-ttu-id="fca70-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fca70-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fca70-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fca70-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fca70-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fca70-152">-DefaultProfile</span></span>
<span data-ttu-id="fca70-153">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fca70-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fca70-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fca70-154">CommonParameters</span></span>
<span data-ttu-id="fca70-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fca70-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fca70-156">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fca70-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fca70-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fca70-157">INPUTS</span></span>

## <span data-ttu-id="fca70-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fca70-158">OUTPUTS</span></span>

### <span data-ttu-id="fca70-159">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fca70-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="fca70-160">Note</span><span class="sxs-lookup"><span data-stu-id="fca70-160">NOTES</span></span>

## <span data-ttu-id="fca70-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fca70-161">RELATED LINKS</span></span>

[<span data-ttu-id="fca70-162">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fca70-162">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="fca70-163">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="fca70-163">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="fca70-164">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="fca70-164">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="fca70-165">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fca70-165">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="fca70-166">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fca70-166">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

