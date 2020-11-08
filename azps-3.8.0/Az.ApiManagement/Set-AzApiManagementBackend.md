---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: 30947e52e5a7afaa8bf2890b95f48f6bb6f36bce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021817"
---
# <span data-ttu-id="084d9-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="084d9-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="084d9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="084d9-102">SYNOPSIS</span></span>
<span data-ttu-id="084d9-103">Aggiorna un backend.</span><span class="sxs-lookup"><span data-stu-id="084d9-103">Updates a Backend.</span></span>

## <span data-ttu-id="084d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="084d9-104">SYNTAX</span></span>

### <span data-ttu-id="084d9-105">ContextParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="084d9-105">ContextParameterSet (Default)</span></span>
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="084d9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="084d9-106">ByInputObject</span></span>
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="084d9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="084d9-107">DESCRIPTION</span></span>
<span data-ttu-id="084d9-108">Aggiorna un backend esistente nella gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="084d9-108">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="084d9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="084d9-109">EXAMPLES</span></span>

### <span data-ttu-id="084d9-110">Aggiorna la descrizione del backend 123</span><span class="sxs-lookup"><span data-stu-id="084d9-110">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="084d9-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="084d9-111">PARAMETERS</span></span>

### <span data-ttu-id="084d9-112">-BackendId</span><span class="sxs-lookup"><span data-stu-id="084d9-112">-BackendId</span></span>
<span data-ttu-id="084d9-113">Identificatore del nuovo backend.</span><span class="sxs-lookup"><span data-stu-id="084d9-113">Identifier of new backend.</span></span>
<span data-ttu-id="084d9-114">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="084d9-114">This parameter is required.</span></span>

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

### <span data-ttu-id="084d9-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="084d9-115">-Context</span></span>
<span data-ttu-id="084d9-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="084d9-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="084d9-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="084d9-117">This parameter is required.</span></span>

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

### <span data-ttu-id="084d9-118">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="084d9-118">-Credential</span></span>
<span data-ttu-id="084d9-119">Dettagli delle credenziali che dovrebbero essere usati per comunicare con il backend.</span><span class="sxs-lookup"><span data-stu-id="084d9-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="084d9-120">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="084d9-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="084d9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="084d9-121">-DefaultProfile</span></span>
<span data-ttu-id="084d9-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="084d9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="084d9-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="084d9-123">-Description</span></span>
<span data-ttu-id="084d9-124">Descrizione del backend.</span><span class="sxs-lookup"><span data-stu-id="084d9-124">Backend Description.</span></span>
<span data-ttu-id="084d9-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="084d9-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="084d9-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="084d9-126">-InputObject</span></span>
<span data-ttu-id="084d9-127">Istanza di PsApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="084d9-127">Instance of PsApiManagementBackend.</span></span> <span data-ttu-id="084d9-128">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="084d9-128">This parameter is required.</span></span>

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

### <span data-ttu-id="084d9-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="084d9-129">-PassThru</span></span>
<span data-ttu-id="084d9-130">Indica che questo cmdlet restituisce il  **PsApiManagementBackend** modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="084d9-130">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="084d9-131">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="084d9-131">-Protocol</span></span>
<span data-ttu-id="084d9-132">Protocollo di comunicazione backend (http o SOAP).</span><span class="sxs-lookup"><span data-stu-id="084d9-132">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="084d9-133">Questo parametro è facoltativo</span><span class="sxs-lookup"><span data-stu-id="084d9-133">This parameter is optional</span></span>

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

### <span data-ttu-id="084d9-134">-Proxy</span><span class="sxs-lookup"><span data-stu-id="084d9-134">-Proxy</span></span>
<span data-ttu-id="084d9-135">Dettagli del server proxy da usare durante l'invio di una richiesta al backend.</span><span class="sxs-lookup"><span data-stu-id="084d9-135">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="084d9-136">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="084d9-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="084d9-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="084d9-137">-ResourceId</span></span>
<span data-ttu-id="084d9-138">URI di gestione della risorsa nel sistema esterno.</span><span class="sxs-lookup"><span data-stu-id="084d9-138">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="084d9-139">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="084d9-139">This parameter is optional.</span></span>
<span data-ttu-id="084d9-140">Questo URL può essere l'ID delle risorse ARM delle app logiche, delle app funzioni o delle app API.</span><span class="sxs-lookup"><span data-stu-id="084d9-140">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="084d9-141">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="084d9-141">-ServiceFabricCluster</span></span>
<span data-ttu-id="084d9-142">Dettagli del backend del cluster del servizio Fabric.</span><span class="sxs-lookup"><span data-stu-id="084d9-142">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="084d9-143">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="084d9-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="084d9-144">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="084d9-144">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="084d9-145">Se ignorare la convalida della catena di certificati quando si parla con il backend.</span><span class="sxs-lookup"><span data-stu-id="084d9-145">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="084d9-146">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="084d9-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="084d9-147">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="084d9-147">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="084d9-148">Se ignorare la convalida del nome del certificato quando si parla con il backend.</span><span class="sxs-lookup"><span data-stu-id="084d9-148">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="084d9-149">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="084d9-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="084d9-150">-Titolo</span><span class="sxs-lookup"><span data-stu-id="084d9-150">-Title</span></span>
<span data-ttu-id="084d9-151">Titolo del backend.</span><span class="sxs-lookup"><span data-stu-id="084d9-151">Backend Title.</span></span>
<span data-ttu-id="084d9-152">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="084d9-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="084d9-153">-URL</span><span class="sxs-lookup"><span data-stu-id="084d9-153">-Url</span></span>
<span data-ttu-id="084d9-154">URL di runtime per il backend.</span><span class="sxs-lookup"><span data-stu-id="084d9-154">Runtime Url for the Backend.</span></span>
<span data-ttu-id="084d9-155">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="084d9-155">This parameter is optional.</span></span>

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

### <span data-ttu-id="084d9-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="084d9-156">-Confirm</span></span>
<span data-ttu-id="084d9-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="084d9-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="084d9-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="084d9-158">-WhatIf</span></span>
<span data-ttu-id="084d9-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="084d9-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="084d9-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="084d9-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="084d9-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="084d9-161">CommonParameters</span></span>
<span data-ttu-id="084d9-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="084d9-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="084d9-163">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="084d9-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="084d9-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="084d9-164">INPUTS</span></span>

### <span data-ttu-id="084d9-165">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="084d9-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="084d9-166">System. String</span><span class="sxs-lookup"><span data-stu-id="084d9-166">System.String</span></span>

### <span data-ttu-id="084d9-167">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="084d9-167">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="084d9-168">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="084d9-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="084d9-169">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="084d9-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="084d9-170">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="084d9-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="084d9-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="084d9-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="084d9-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="084d9-172">OUTPUTS</span></span>

### <span data-ttu-id="084d9-173">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="084d9-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="084d9-174">Note</span><span class="sxs-lookup"><span data-stu-id="084d9-174">NOTES</span></span>

## <span data-ttu-id="084d9-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="084d9-175">RELATED LINKS</span></span>

[<span data-ttu-id="084d9-176">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="084d9-176">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="084d9-177">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="084d9-177">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="084d9-178">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="084d9-178">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="084d9-179">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="084d9-179">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="084d9-180">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="084d9-180">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
