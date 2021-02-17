---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: 8631120178a256aa1ec5b817727f9362f6d8f076
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407285"
---
# <span data-ttu-id="d12ab-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d12ab-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="d12ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d12ab-102">SYNOPSIS</span></span>
<span data-ttu-id="d12ab-103">Aggiorna un back-end.</span><span class="sxs-lookup"><span data-stu-id="d12ab-103">Updates a Backend.</span></span>

## <span data-ttu-id="d12ab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d12ab-104">SYNTAX</span></span>

### <span data-ttu-id="d12ab-105">ContextParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d12ab-105">ContextParameterSet (Default)</span></span>
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d12ab-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d12ab-106">ByInputObject</span></span>
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d12ab-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d12ab-107">DESCRIPTION</span></span>
<span data-ttu-id="d12ab-108">Aggiorna un back-end esistente in Gestione API.</span><span class="sxs-lookup"><span data-stu-id="d12ab-108">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="d12ab-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d12ab-109">EXAMPLES</span></span>

### <span data-ttu-id="d12ab-110">Aggiorna la descrizione del back-end 123</span><span class="sxs-lookup"><span data-stu-id="d12ab-110">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="d12ab-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d12ab-111">PARAMETERS</span></span>

### <span data-ttu-id="d12ab-112">-BackendId</span><span class="sxs-lookup"><span data-stu-id="d12ab-112">-BackendId</span></span>
<span data-ttu-id="d12ab-113">Identificatore del nuovo back-end.</span><span class="sxs-lookup"><span data-stu-id="d12ab-113">Identifier of new backend.</span></span>
<span data-ttu-id="d12ab-114">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d12ab-114">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d12ab-115">-Context</span><span class="sxs-lookup"><span data-stu-id="d12ab-115">-Context</span></span>
<span data-ttu-id="d12ab-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d12ab-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d12ab-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d12ab-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d12ab-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="d12ab-118">-Credential</span></span>
<span data-ttu-id="d12ab-119">Dettagli delle credenziali che devono essere usati quando si parla con il back-end.</span><span class="sxs-lookup"><span data-stu-id="d12ab-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="d12ab-120">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d12ab-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="d12ab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d12ab-121">-DefaultProfile</span></span>
<span data-ttu-id="d12ab-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d12ab-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d12ab-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="d12ab-123">-Description</span></span>
<span data-ttu-id="d12ab-124">Descrizione back-end.</span><span class="sxs-lookup"><span data-stu-id="d12ab-124">Backend Description.</span></span>
<span data-ttu-id="d12ab-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d12ab-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="d12ab-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d12ab-126">-InputObject</span></span>
<span data-ttu-id="d12ab-127">Istanza di PsApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="d12ab-127">Instance of PsApiManagementBackend.</span></span> <span data-ttu-id="d12ab-128">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d12ab-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d12ab-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d12ab-129">-PassThru</span></span>
<span data-ttu-id="d12ab-130">Indica che questo cmdlet restituisce  **PsApiManagementBackend** che il cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="d12ab-130">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d12ab-131">-Protocol</span><span class="sxs-lookup"><span data-stu-id="d12ab-131">-Protocol</span></span>
<span data-ttu-id="d12ab-132">Protocollo Backend Communication (http o soap).</span><span class="sxs-lookup"><span data-stu-id="d12ab-132">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="d12ab-133">Questo parametro è facoltativo</span><span class="sxs-lookup"><span data-stu-id="d12ab-133">This parameter is optional</span></span>

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

### <span data-ttu-id="d12ab-134">-Proxy</span><span class="sxs-lookup"><span data-stu-id="d12ab-134">-Proxy</span></span>
<span data-ttu-id="d12ab-135">Dettagli del server Proxy da usare durante l'invio di una richiesta al back-end.</span><span class="sxs-lookup"><span data-stu-id="d12ab-135">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="d12ab-136">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d12ab-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="d12ab-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d12ab-137">-ResourceId</span></span>
<span data-ttu-id="d12ab-138">Uri gestione della risorsa nel sistema esterno.</span><span class="sxs-lookup"><span data-stu-id="d12ab-138">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="d12ab-139">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d12ab-139">This parameter is optional.</span></span>
<span data-ttu-id="d12ab-140">Questo URL può essere l'ID risorsa Arm di App logica, app per funzioni o app Api.</span><span class="sxs-lookup"><span data-stu-id="d12ab-140">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="d12ab-141">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="d12ab-141">-ServiceFabricCluster</span></span>
<span data-ttu-id="d12ab-142">Dettagli back-end del cluster Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="d12ab-142">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="d12ab-143">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d12ab-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="d12ab-144">-SkipCertificateChainValid</span><span class="sxs-lookup"><span data-stu-id="d12ab-144">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="d12ab-145">Se ignorare la convalida della catena di certificati quando si parla con il back-end.</span><span class="sxs-lookup"><span data-stu-id="d12ab-145">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="d12ab-146">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d12ab-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="d12ab-147">-SkipCertificateNameValid</span><span class="sxs-lookup"><span data-stu-id="d12ab-147">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="d12ab-148">Se ignorare la convalida del nome del certificato quando si parla con il back-end.</span><span class="sxs-lookup"><span data-stu-id="d12ab-148">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="d12ab-149">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d12ab-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="d12ab-150">-Title</span><span class="sxs-lookup"><span data-stu-id="d12ab-150">-Title</span></span>
<span data-ttu-id="d12ab-151">Titolo back-end.</span><span class="sxs-lookup"><span data-stu-id="d12ab-151">Backend Title.</span></span>
<span data-ttu-id="d12ab-152">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d12ab-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="d12ab-153">-URL</span><span class="sxs-lookup"><span data-stu-id="d12ab-153">-Url</span></span>
<span data-ttu-id="d12ab-154">URL di runtime per il back-end.</span><span class="sxs-lookup"><span data-stu-id="d12ab-154">Runtime Url for the Backend.</span></span>
<span data-ttu-id="d12ab-155">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d12ab-155">This parameter is optional.</span></span>

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

### <span data-ttu-id="d12ab-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d12ab-156">-Confirm</span></span>
<span data-ttu-id="d12ab-157">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d12ab-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d12ab-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d12ab-158">-WhatIf</span></span>
<span data-ttu-id="d12ab-159">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d12ab-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d12ab-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d12ab-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d12ab-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d12ab-161">CommonParameters</span></span>
<span data-ttu-id="d12ab-162">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d12ab-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d12ab-163">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d12ab-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d12ab-164">INPUT</span><span class="sxs-lookup"><span data-stu-id="d12ab-164">INPUTS</span></span>

### <span data-ttu-id="d12ab-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d12ab-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d12ab-166">System.String</span><span class="sxs-lookup"><span data-stu-id="d12ab-166">System.String</span></span>

### <span data-ttu-id="d12ab-167">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d12ab-167">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d12ab-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="d12ab-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="d12ab-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="d12ab-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="d12ab-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d12ab-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="d12ab-171">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d12ab-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d12ab-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d12ab-172">OUTPUTS</span></span>

### <span data-ttu-id="d12ab-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d12ab-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="d12ab-174">NOTE</span><span class="sxs-lookup"><span data-stu-id="d12ab-174">NOTES</span></span>

## <span data-ttu-id="d12ab-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d12ab-175">RELATED LINKS</span></span>

[<span data-ttu-id="d12ab-176">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d12ab-176">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="d12ab-177">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d12ab-177">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="d12ab-178">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="d12ab-178">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="d12ab-179">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="d12ab-179">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="d12ab-180">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d12ab-180">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
