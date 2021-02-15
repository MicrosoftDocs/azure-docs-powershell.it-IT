---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: 0ac89ed099029fbbabe90e07da7ba9c204449db9
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400740"
---
# <span data-ttu-id="eaba2-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="eaba2-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="eaba2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaba2-102">SYNOPSIS</span></span>
<span data-ttu-id="eaba2-103">Aggiorna un back-end.</span><span class="sxs-lookup"><span data-stu-id="eaba2-103">Updates a Backend.</span></span>

## <span data-ttu-id="eaba2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eaba2-104">SYNTAX</span></span>

```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaba2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="eaba2-105">DESCRIPTION</span></span>
<span data-ttu-id="eaba2-106">Aggiorna un back-end esistente in Gestione API.</span><span class="sxs-lookup"><span data-stu-id="eaba2-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="eaba2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eaba2-107">EXAMPLES</span></span>

### <span data-ttu-id="eaba2-108">Aggiorna la descrizione del back-end 123</span><span class="sxs-lookup"><span data-stu-id="eaba2-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="eaba2-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eaba2-109">PARAMETERS</span></span>

### <span data-ttu-id="eaba2-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="eaba2-110">-BackendId</span></span>
<span data-ttu-id="eaba2-111">Identificatore del nuovo back-end.</span><span class="sxs-lookup"><span data-stu-id="eaba2-111">Identifier of new backend.</span></span>
<span data-ttu-id="eaba2-112">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="eaba2-112">This parameter is required.</span></span>

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

### <span data-ttu-id="eaba2-113">-Context</span><span class="sxs-lookup"><span data-stu-id="eaba2-113">-Context</span></span>
<span data-ttu-id="eaba2-114">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="eaba2-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="eaba2-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="eaba2-115">This parameter is required.</span></span>

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

### <span data-ttu-id="eaba2-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="eaba2-116">-Credential</span></span>
<span data-ttu-id="eaba2-117">Dettagli delle credenziali che devono essere usati quando si parla con il back-end.</span><span class="sxs-lookup"><span data-stu-id="eaba2-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="eaba2-118">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="eaba2-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="eaba2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaba2-119">-DefaultProfile</span></span>
<span data-ttu-id="eaba2-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eaba2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaba2-121">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="eaba2-121">-Description</span></span>
<span data-ttu-id="eaba2-122">Descrizione back-end.</span><span class="sxs-lookup"><span data-stu-id="eaba2-122">Backend Description.</span></span>
<span data-ttu-id="eaba2-123">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="eaba2-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="eaba2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eaba2-124">-PassThru</span></span>
<span data-ttu-id="eaba2-125">Indica che questo cmdlet restituisce  **PsApiManagementBackend** che il cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="eaba2-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="eaba2-126">-Protocol</span><span class="sxs-lookup"><span data-stu-id="eaba2-126">-Protocol</span></span>
<span data-ttu-id="eaba2-127">Protocollo Backend Communication (http o soap).</span><span class="sxs-lookup"><span data-stu-id="eaba2-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="eaba2-128">Questo parametro è facoltativo</span><span class="sxs-lookup"><span data-stu-id="eaba2-128">This parameter is optional</span></span>

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

### <span data-ttu-id="eaba2-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="eaba2-129">-Proxy</span></span>
<span data-ttu-id="eaba2-130">Dettagli del server Proxy da usare durante l'invio di una richiesta al back-end.</span><span class="sxs-lookup"><span data-stu-id="eaba2-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="eaba2-131">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="eaba2-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="eaba2-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eaba2-132">-ResourceId</span></span>
<span data-ttu-id="eaba2-133">Uri gestione della risorsa nel sistema esterno.</span><span class="sxs-lookup"><span data-stu-id="eaba2-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="eaba2-134">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="eaba2-134">This parameter is optional.</span></span>
<span data-ttu-id="eaba2-135">Questo URL può essere l'ID risorsa Arm di App logica, app per funzioni o app Api.</span><span class="sxs-lookup"><span data-stu-id="eaba2-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="eaba2-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="eaba2-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="eaba2-137">Dettagli back-end del cluster Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="eaba2-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="eaba2-138">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="eaba2-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="eaba2-139">-SkipCertificateChainValid</span><span class="sxs-lookup"><span data-stu-id="eaba2-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="eaba2-140">Se ignorare la convalida della catena di certificati quando si parla con il back-end.</span><span class="sxs-lookup"><span data-stu-id="eaba2-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="eaba2-141">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="eaba2-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="eaba2-142">-SkipCertificateNameValid</span><span class="sxs-lookup"><span data-stu-id="eaba2-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="eaba2-143">Se ignorare la convalida del nome del certificato quando si parla con il back-end.</span><span class="sxs-lookup"><span data-stu-id="eaba2-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="eaba2-144">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="eaba2-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="eaba2-145">-Title</span><span class="sxs-lookup"><span data-stu-id="eaba2-145">-Title</span></span>
<span data-ttu-id="eaba2-146">Titolo back-end.</span><span class="sxs-lookup"><span data-stu-id="eaba2-146">Backend Title.</span></span>
<span data-ttu-id="eaba2-147">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="eaba2-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="eaba2-148">-URL</span><span class="sxs-lookup"><span data-stu-id="eaba2-148">-Url</span></span>
<span data-ttu-id="eaba2-149">URL di runtime per il back-end.</span><span class="sxs-lookup"><span data-stu-id="eaba2-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="eaba2-150">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="eaba2-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="eaba2-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eaba2-151">-Confirm</span></span>
<span data-ttu-id="eaba2-152">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eaba2-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaba2-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaba2-153">-WhatIf</span></span>
<span data-ttu-id="eaba2-154">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eaba2-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eaba2-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eaba2-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaba2-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaba2-156">CommonParameters</span></span>
<span data-ttu-id="eaba2-157">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaba2-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaba2-158">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaba2-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaba2-159">INPUT</span><span class="sxs-lookup"><span data-stu-id="eaba2-159">INPUTS</span></span>

### <span data-ttu-id="eaba2-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="eaba2-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="eaba2-161">System.String</span><span class="sxs-lookup"><span data-stu-id="eaba2-161">System.String</span></span>

### <span data-ttu-id="eaba2-162">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="eaba2-162">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="eaba2-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="eaba2-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="eaba2-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="eaba2-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="eaba2-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="eaba2-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="eaba2-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="eaba2-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="eaba2-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eaba2-167">OUTPUTS</span></span>

### <span data-ttu-id="eaba2-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="eaba2-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="eaba2-169">NOTE</span><span class="sxs-lookup"><span data-stu-id="eaba2-169">NOTES</span></span>

## <span data-ttu-id="eaba2-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eaba2-170">RELATED LINKS</span></span>

[<span data-ttu-id="eaba2-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="eaba2-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="eaba2-172">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="eaba2-172">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="eaba2-173">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="eaba2-173">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="eaba2-174">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="eaba2-174">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="eaba2-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="eaba2-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
