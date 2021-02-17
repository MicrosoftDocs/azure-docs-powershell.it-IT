---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: f26cb91ef820df6dfa67a0fb5664d4607df8fb21
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399465"
---
# <span data-ttu-id="66e83-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="66e83-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="66e83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66e83-102">SYNOPSIS</span></span>
<span data-ttu-id="66e83-103">Crea una nuova entità back-end.</span><span class="sxs-lookup"><span data-stu-id="66e83-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="66e83-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="66e83-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66e83-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="66e83-105">DESCRIPTION</span></span>
<span data-ttu-id="66e83-106">Crea una nuova entità back-end in Gestione api.</span><span class="sxs-lookup"><span data-stu-id="66e83-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="66e83-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="66e83-107">EXAMPLES</span></span>

### <span data-ttu-id="66e83-108">Creare back-end 123 con uno schema di autorizzazione di base</span><span class="sxs-lookup"><span data-stu-id="66e83-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="66e83-109">Crea un nuovo back-end</span><span class="sxs-lookup"><span data-stu-id="66e83-109">Creates a new Backend</span></span>

## <span data-ttu-id="66e83-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66e83-110">PARAMETERS</span></span>

### <span data-ttu-id="66e83-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="66e83-111">-BackendId</span></span>
<span data-ttu-id="66e83-112">Identificatore del nuovo back-end.</span><span class="sxs-lookup"><span data-stu-id="66e83-112">Identifier of new backend.</span></span>
<span data-ttu-id="66e83-113">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="66e83-113">This parameter is optional.</span></span>
<span data-ttu-id="66e83-114">Se non viene specificato, verrà generato.</span><span class="sxs-lookup"><span data-stu-id="66e83-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="66e83-115">-Context</span><span class="sxs-lookup"><span data-stu-id="66e83-115">-Context</span></span>
<span data-ttu-id="66e83-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="66e83-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="66e83-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="66e83-117">This parameter is required.</span></span>

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

### <span data-ttu-id="66e83-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="66e83-118">-Credential</span></span>
<span data-ttu-id="66e83-119">Dettagli delle credenziali che devono essere usati quando si parla con il back-end.</span><span class="sxs-lookup"><span data-stu-id="66e83-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="66e83-120">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="66e83-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="66e83-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66e83-121">-DefaultProfile</span></span>
<span data-ttu-id="66e83-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="66e83-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66e83-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="66e83-123">-Description</span></span>
<span data-ttu-id="66e83-124">Descrizione back-end.</span><span class="sxs-lookup"><span data-stu-id="66e83-124">Backend Description.</span></span>
<span data-ttu-id="66e83-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="66e83-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="66e83-126">-Protocol</span><span class="sxs-lookup"><span data-stu-id="66e83-126">-Protocol</span></span>
<span data-ttu-id="66e83-127">Protocollo Back-End Communication.</span><span class="sxs-lookup"><span data-stu-id="66e83-127">Backend Communication protocol.</span></span>
<span data-ttu-id="66e83-128">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="66e83-128">This parameter is required.</span></span>
<span data-ttu-id="66e83-129">I valori validi sono "http" e "soap".</span><span class="sxs-lookup"><span data-stu-id="66e83-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="66e83-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="66e83-130">-Proxy</span></span>
<span data-ttu-id="66e83-131">Dettagli del server proxy da usare durante l'invio di una richiesta al back-end.</span><span class="sxs-lookup"><span data-stu-id="66e83-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="66e83-132">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="66e83-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="66e83-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66e83-133">-ResourceId</span></span>
<span data-ttu-id="66e83-134">Uri gestione della risorsa nel sistema esterno.</span><span class="sxs-lookup"><span data-stu-id="66e83-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="66e83-135">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="66e83-135">This parameter is optional.</span></span>
<span data-ttu-id="66e83-136">Questo URL può essere l'ID risorsa Arm di App logica, App per funzioni o App Api.</span><span class="sxs-lookup"><span data-stu-id="66e83-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="66e83-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="66e83-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="66e83-138">Dettagli back-end del cluster Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="66e83-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="66e83-139">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="66e83-139">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e83-140">-SkipCertificateChainValid</span><span class="sxs-lookup"><span data-stu-id="66e83-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="66e83-141">Se ignorare la convalida della catena di certificati quando si parla con il back-end.</span><span class="sxs-lookup"><span data-stu-id="66e83-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="66e83-142">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="66e83-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="66e83-143">-SkipCertificateNameValid</span><span class="sxs-lookup"><span data-stu-id="66e83-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="66e83-144">Se ignorare la convalida del nome del certificato quando si parla con il back-end.</span><span class="sxs-lookup"><span data-stu-id="66e83-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="66e83-145">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="66e83-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="66e83-146">-Title</span><span class="sxs-lookup"><span data-stu-id="66e83-146">-Title</span></span>
<span data-ttu-id="66e83-147">Titolo back-end.</span><span class="sxs-lookup"><span data-stu-id="66e83-147">Backend Title.</span></span>
<span data-ttu-id="66e83-148">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="66e83-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="66e83-149">-URL</span><span class="sxs-lookup"><span data-stu-id="66e83-149">-Url</span></span>
<span data-ttu-id="66e83-150">URL di runtime per il back-end.</span><span class="sxs-lookup"><span data-stu-id="66e83-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="66e83-151">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="66e83-151">This parameter is required.</span></span>

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

### <span data-ttu-id="66e83-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66e83-152">-Confirm</span></span>
<span data-ttu-id="66e83-153">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66e83-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66e83-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66e83-154">-WhatIf</span></span>
<span data-ttu-id="66e83-155">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66e83-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66e83-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66e83-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66e83-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66e83-157">CommonParameters</span></span>
<span data-ttu-id="66e83-158">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66e83-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66e83-159">Per altre informazioni, [vedere](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="66e83-159">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66e83-160">INPUT</span><span class="sxs-lookup"><span data-stu-id="66e83-160">INPUTS</span></span>

### <span data-ttu-id="66e83-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="66e83-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="66e83-162">System.String</span><span class="sxs-lookup"><span data-stu-id="66e83-162">System.String</span></span>

### <span data-ttu-id="66e83-163">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="66e83-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="66e83-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="66e83-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="66e83-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="66e83-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="66e83-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="66e83-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="66e83-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="66e83-167">OUTPUTS</span></span>

### <span data-ttu-id="66e83-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="66e83-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="66e83-169">NOTE</span><span class="sxs-lookup"><span data-stu-id="66e83-169">NOTES</span></span>

## <span data-ttu-id="66e83-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="66e83-170">RELATED LINKS</span></span>

[<span data-ttu-id="66e83-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="66e83-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="66e83-172">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="66e83-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="66e83-173">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="66e83-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="66e83-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="66e83-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="66e83-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="66e83-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

