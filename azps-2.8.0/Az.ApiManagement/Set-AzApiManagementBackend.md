---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: cb7348e31ca80834836b27c97aa7f68e4207ed24
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404327"
---
# <span data-ttu-id="80491-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="80491-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="80491-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80491-102">SYNOPSIS</span></span>
<span data-ttu-id="80491-103">Aggiorna un back-end.</span><span class="sxs-lookup"><span data-stu-id="80491-103">Updates a Backend.</span></span>

## <span data-ttu-id="80491-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80491-104">SYNTAX</span></span>

### <span data-ttu-id="80491-105">ContextParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="80491-105">ContextParameterSet (Default)</span></span>
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80491-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="80491-106">ByInputObject</span></span>
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80491-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="80491-107">DESCRIPTION</span></span>
<span data-ttu-id="80491-108">Aggiorna un back-end esistente in Gestione API.</span><span class="sxs-lookup"><span data-stu-id="80491-108">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="80491-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80491-109">EXAMPLES</span></span>

### <span data-ttu-id="80491-110">Aggiorna la descrizione del back-end 123</span><span class="sxs-lookup"><span data-stu-id="80491-110">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="80491-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80491-111">PARAMETERS</span></span>

### <span data-ttu-id="80491-112">-BackendId</span><span class="sxs-lookup"><span data-stu-id="80491-112">-BackendId</span></span>
<span data-ttu-id="80491-113">Identificatore del nuovo back-end.</span><span class="sxs-lookup"><span data-stu-id="80491-113">Identifier of new backend.</span></span>
<span data-ttu-id="80491-114">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="80491-114">This parameter is required.</span></span>

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

### <span data-ttu-id="80491-115">-Context</span><span class="sxs-lookup"><span data-stu-id="80491-115">-Context</span></span>
<span data-ttu-id="80491-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="80491-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="80491-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="80491-117">This parameter is required.</span></span>

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

### <span data-ttu-id="80491-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="80491-118">-Credential</span></span>
<span data-ttu-id="80491-119">Dettagli delle credenziali che devono essere usati quando si parla con il back-end.</span><span class="sxs-lookup"><span data-stu-id="80491-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="80491-120">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="80491-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="80491-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80491-121">-DefaultProfile</span></span>
<span data-ttu-id="80491-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="80491-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80491-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="80491-123">-Description</span></span>
<span data-ttu-id="80491-124">Descrizione back-end.</span><span class="sxs-lookup"><span data-stu-id="80491-124">Backend Description.</span></span>
<span data-ttu-id="80491-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="80491-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="80491-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80491-126">-InputObject</span></span>
<span data-ttu-id="80491-127">Istanza di PsApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="80491-127">Instance of PsApiManagementBackend.</span></span> <span data-ttu-id="80491-128">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="80491-128">This parameter is required.</span></span>

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

### <span data-ttu-id="80491-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80491-129">-PassThru</span></span>
<span data-ttu-id="80491-130">Indica che questo cmdlet restituisce  **PsApiManagementBackend** che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="80491-130">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="80491-131">-Protocol</span><span class="sxs-lookup"><span data-stu-id="80491-131">-Protocol</span></span>
<span data-ttu-id="80491-132">Protocollo Backend Communication (http o soap).</span><span class="sxs-lookup"><span data-stu-id="80491-132">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="80491-133">Questo parametro è facoltativo</span><span class="sxs-lookup"><span data-stu-id="80491-133">This parameter is optional</span></span>

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

### <span data-ttu-id="80491-134">-Proxy</span><span class="sxs-lookup"><span data-stu-id="80491-134">-Proxy</span></span>
<span data-ttu-id="80491-135">Dettagli del server proxy da usare durante l'invio di una richiesta al back-end.</span><span class="sxs-lookup"><span data-stu-id="80491-135">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="80491-136">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="80491-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="80491-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80491-137">-ResourceId</span></span>
<span data-ttu-id="80491-138">Uri gestione della risorsa nel sistema esterno.</span><span class="sxs-lookup"><span data-stu-id="80491-138">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="80491-139">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="80491-139">This parameter is optional.</span></span>
<span data-ttu-id="80491-140">Questo URL può essere l'ID risorsa Arm di App logica, App per funzioni o App Api.</span><span class="sxs-lookup"><span data-stu-id="80491-140">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="80491-141">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="80491-141">-ServiceFabricCluster</span></span>
<span data-ttu-id="80491-142">Dettagli back-end del cluster Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="80491-142">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="80491-143">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="80491-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="80491-144">-SkipCertificateChainValid</span><span class="sxs-lookup"><span data-stu-id="80491-144">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="80491-145">Se ignorare la convalida della catena di certificati quando si parla con il back-end.</span><span class="sxs-lookup"><span data-stu-id="80491-145">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="80491-146">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="80491-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="80491-147">-SkipCertificateNameValid</span><span class="sxs-lookup"><span data-stu-id="80491-147">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="80491-148">Se ignorare la convalida del nome del certificato quando si parla con il back-end.</span><span class="sxs-lookup"><span data-stu-id="80491-148">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="80491-149">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="80491-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="80491-150">-Title</span><span class="sxs-lookup"><span data-stu-id="80491-150">-Title</span></span>
<span data-ttu-id="80491-151">Titolo back-end.</span><span class="sxs-lookup"><span data-stu-id="80491-151">Backend Title.</span></span>
<span data-ttu-id="80491-152">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="80491-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="80491-153">-URL</span><span class="sxs-lookup"><span data-stu-id="80491-153">-Url</span></span>
<span data-ttu-id="80491-154">URL di runtime per il back-end.</span><span class="sxs-lookup"><span data-stu-id="80491-154">Runtime Url for the Backend.</span></span>
<span data-ttu-id="80491-155">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="80491-155">This parameter is optional.</span></span>

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

### <span data-ttu-id="80491-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80491-156">-Confirm</span></span>
<span data-ttu-id="80491-157">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80491-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80491-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80491-158">-WhatIf</span></span>
<span data-ttu-id="80491-159">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80491-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80491-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80491-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80491-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80491-161">CommonParameters</span></span>
<span data-ttu-id="80491-162">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80491-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80491-163">Per altre informazioni, [vedere](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="80491-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80491-164">INPUT</span><span class="sxs-lookup"><span data-stu-id="80491-164">INPUTS</span></span>

### <span data-ttu-id="80491-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="80491-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="80491-166">System.String</span><span class="sxs-lookup"><span data-stu-id="80491-166">System.String</span></span>

### <span data-ttu-id="80491-167">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="80491-167">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="80491-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="80491-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="80491-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="80491-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="80491-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="80491-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="80491-171">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="80491-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="80491-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80491-172">OUTPUTS</span></span>

### <span data-ttu-id="80491-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="80491-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="80491-174">NOTE</span><span class="sxs-lookup"><span data-stu-id="80491-174">NOTES</span></span>

## <span data-ttu-id="80491-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80491-175">RELATED LINKS</span></span>

[<span data-ttu-id="80491-176">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="80491-176">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="80491-177">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="80491-177">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="80491-178">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="80491-178">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="80491-179">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="80491-179">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="80491-180">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="80491-180">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
