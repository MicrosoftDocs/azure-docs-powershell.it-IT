---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: cd9ce1d65a2adf13f0f33620ba41b75f394011b4
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405415"
---
# <span data-ttu-id="09d4d-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="09d4d-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="09d4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09d4d-102">SYNOPSIS</span></span>
<span data-ttu-id="09d4d-103">Crea una nuova entità back-end.</span><span class="sxs-lookup"><span data-stu-id="09d4d-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="09d4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09d4d-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09d4d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="09d4d-105">DESCRIPTION</span></span>
<span data-ttu-id="09d4d-106">Crea una nuova entità back-end in Gestione API.</span><span class="sxs-lookup"><span data-stu-id="09d4d-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="09d4d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09d4d-107">EXAMPLES</span></span>

### <span data-ttu-id="09d4d-108">Creare back-end 123 con uno schema di autorizzazione di base</span><span class="sxs-lookup"><span data-stu-id="09d4d-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="09d4d-109">Crea un nuovo back-end</span><span class="sxs-lookup"><span data-stu-id="09d4d-109">Creates a new Backend</span></span>

## <span data-ttu-id="09d4d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09d4d-110">PARAMETERS</span></span>

### <span data-ttu-id="09d4d-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="09d4d-111">-BackendId</span></span>
<span data-ttu-id="09d4d-112">Identificatore del nuovo back-end.</span><span class="sxs-lookup"><span data-stu-id="09d4d-112">Identifier of new backend.</span></span>
<span data-ttu-id="09d4d-113">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="09d4d-113">This parameter is optional.</span></span>
<span data-ttu-id="09d4d-114">Se non viene specificato, verrà generato.</span><span class="sxs-lookup"><span data-stu-id="09d4d-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="09d4d-115">-Context</span><span class="sxs-lookup"><span data-stu-id="09d4d-115">-Context</span></span>
<span data-ttu-id="09d4d-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="09d4d-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="09d4d-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="09d4d-117">This parameter is required.</span></span>

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

### <span data-ttu-id="09d4d-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="09d4d-118">-Credential</span></span>
<span data-ttu-id="09d4d-119">Dettagli delle credenziali che devono essere usati quando si parla con il back-end.</span><span class="sxs-lookup"><span data-stu-id="09d4d-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="09d4d-120">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="09d4d-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="09d4d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09d4d-121">-DefaultProfile</span></span>
<span data-ttu-id="09d4d-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="09d4d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09d4d-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="09d4d-123">-Description</span></span>
<span data-ttu-id="09d4d-124">Descrizione back-end.</span><span class="sxs-lookup"><span data-stu-id="09d4d-124">Backend Description.</span></span>
<span data-ttu-id="09d4d-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="09d4d-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="09d4d-126">-Protocol</span><span class="sxs-lookup"><span data-stu-id="09d4d-126">-Protocol</span></span>
<span data-ttu-id="09d4d-127">Protocollo Back-End Communication.</span><span class="sxs-lookup"><span data-stu-id="09d4d-127">Backend Communication protocol.</span></span>
<span data-ttu-id="09d4d-128">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="09d4d-128">This parameter is required.</span></span>
<span data-ttu-id="09d4d-129">I valori validi sono "http" e "soap".</span><span class="sxs-lookup"><span data-stu-id="09d4d-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="09d4d-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="09d4d-130">-Proxy</span></span>
<span data-ttu-id="09d4d-131">Dettagli del server Proxy da usare durante l'invio di una richiesta al back-end.</span><span class="sxs-lookup"><span data-stu-id="09d4d-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="09d4d-132">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="09d4d-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="09d4d-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09d4d-133">-ResourceId</span></span>
<span data-ttu-id="09d4d-134">Uri gestione della risorsa nel sistema esterno.</span><span class="sxs-lookup"><span data-stu-id="09d4d-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="09d4d-135">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="09d4d-135">This parameter is optional.</span></span>
<span data-ttu-id="09d4d-136">Questo URL può essere l'ID risorsa Arm di App logica, app per funzioni o app Api.</span><span class="sxs-lookup"><span data-stu-id="09d4d-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="09d4d-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="09d4d-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="09d4d-138">Dettagli back-end del cluster Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="09d4d-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="09d4d-139">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="09d4d-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="09d4d-140">-SkipCertificateChainValid</span><span class="sxs-lookup"><span data-stu-id="09d4d-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="09d4d-141">Se ignorare la convalida della catena di certificati quando si parla con il back-end.</span><span class="sxs-lookup"><span data-stu-id="09d4d-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="09d4d-142">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="09d4d-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="09d4d-143">-SkipCertificateNameValid</span><span class="sxs-lookup"><span data-stu-id="09d4d-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="09d4d-144">Se ignorare la convalida del nome del certificato quando si parla con il back-end.</span><span class="sxs-lookup"><span data-stu-id="09d4d-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="09d4d-145">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="09d4d-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="09d4d-146">-Title</span><span class="sxs-lookup"><span data-stu-id="09d4d-146">-Title</span></span>
<span data-ttu-id="09d4d-147">Titolo back-end.</span><span class="sxs-lookup"><span data-stu-id="09d4d-147">Backend Title.</span></span>
<span data-ttu-id="09d4d-148">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="09d4d-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="09d4d-149">-URL</span><span class="sxs-lookup"><span data-stu-id="09d4d-149">-Url</span></span>
<span data-ttu-id="09d4d-150">URL di runtime per il back-end.</span><span class="sxs-lookup"><span data-stu-id="09d4d-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="09d4d-151">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="09d4d-151">This parameter is required.</span></span>

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

### <span data-ttu-id="09d4d-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09d4d-152">-Confirm</span></span>
<span data-ttu-id="09d4d-153">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09d4d-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09d4d-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09d4d-154">-WhatIf</span></span>
<span data-ttu-id="09d4d-155">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09d4d-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09d4d-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09d4d-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09d4d-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09d4d-157">CommonParameters</span></span>
<span data-ttu-id="09d4d-158">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09d4d-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09d4d-159">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="09d4d-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09d4d-160">INPUT</span><span class="sxs-lookup"><span data-stu-id="09d4d-160">INPUTS</span></span>

### <span data-ttu-id="09d4d-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="09d4d-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="09d4d-162">System.String</span><span class="sxs-lookup"><span data-stu-id="09d4d-162">System.String</span></span>

### <span data-ttu-id="09d4d-163">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="09d4d-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="09d4d-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="09d4d-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="09d4d-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="09d4d-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="09d4d-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="09d4d-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="09d4d-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09d4d-167">OUTPUTS</span></span>

### <span data-ttu-id="09d4d-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="09d4d-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="09d4d-169">NOTE</span><span class="sxs-lookup"><span data-stu-id="09d4d-169">NOTES</span></span>

## <span data-ttu-id="09d4d-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09d4d-170">RELATED LINKS</span></span>

[<span data-ttu-id="09d4d-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="09d4d-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="09d4d-172">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="09d4d-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="09d4d-173">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="09d4d-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="09d4d-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="09d4d-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="09d4d-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="09d4d-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

