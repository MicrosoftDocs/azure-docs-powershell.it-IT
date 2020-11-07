---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: 4886e5e064276b73f571c81724b98a409930126a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673600"
---
# <span data-ttu-id="98dfe-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="98dfe-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="98dfe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="98dfe-102">SYNOPSIS</span></span>
<span data-ttu-id="98dfe-103">Crea una nuova entità back-end.</span><span class="sxs-lookup"><span data-stu-id="98dfe-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="98dfe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98dfe-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98dfe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98dfe-105">DESCRIPTION</span></span>
<span data-ttu-id="98dfe-106">Crea una nuova entità back-end nella gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="98dfe-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="98dfe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98dfe-107">EXAMPLES</span></span>

### <span data-ttu-id="98dfe-108">Creare un backend 123 con uno schema di autorizzazione di base</span><span class="sxs-lookup"><span data-stu-id="98dfe-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="98dfe-109">Crea un nuovo backend</span><span class="sxs-lookup"><span data-stu-id="98dfe-109">Creates a new Backend</span></span>

## <span data-ttu-id="98dfe-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="98dfe-110">PARAMETERS</span></span>

### <span data-ttu-id="98dfe-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="98dfe-111">-BackendId</span></span>
<span data-ttu-id="98dfe-112">Identificatore del nuovo backend.</span><span class="sxs-lookup"><span data-stu-id="98dfe-112">Identifier of new backend.</span></span>
<span data-ttu-id="98dfe-113">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="98dfe-113">This parameter is optional.</span></span>
<span data-ttu-id="98dfe-114">Se non viene specificato verrà generato.</span><span class="sxs-lookup"><span data-stu-id="98dfe-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="98dfe-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="98dfe-115">-Context</span></span>
<span data-ttu-id="98dfe-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="98dfe-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="98dfe-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="98dfe-117">This parameter is required.</span></span>

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

### <span data-ttu-id="98dfe-118">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="98dfe-118">-Credential</span></span>
<span data-ttu-id="98dfe-119">Dettagli delle credenziali che dovrebbero essere usati per comunicare con il backend.</span><span class="sxs-lookup"><span data-stu-id="98dfe-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="98dfe-120">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="98dfe-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="98dfe-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98dfe-121">-DefaultProfile</span></span>
<span data-ttu-id="98dfe-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="98dfe-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98dfe-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="98dfe-123">-Description</span></span>
<span data-ttu-id="98dfe-124">Descrizione del backend.</span><span class="sxs-lookup"><span data-stu-id="98dfe-124">Backend Description.</span></span>
<span data-ttu-id="98dfe-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="98dfe-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="98dfe-126">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="98dfe-126">-Protocol</span></span>
<span data-ttu-id="98dfe-127">Protocollo di comunicazione backend.</span><span class="sxs-lookup"><span data-stu-id="98dfe-127">Backend Communication protocol.</span></span>
<span data-ttu-id="98dfe-128">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="98dfe-128">This parameter is required.</span></span>
<span data-ttu-id="98dfe-129">I valori validi sono "http" e "SOAP".</span><span class="sxs-lookup"><span data-stu-id="98dfe-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="98dfe-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="98dfe-130">-Proxy</span></span>
<span data-ttu-id="98dfe-131">Dettagli del server proxy da usare durante l'invio di una richiesta al backend.</span><span class="sxs-lookup"><span data-stu-id="98dfe-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="98dfe-132">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="98dfe-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="98dfe-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98dfe-133">-ResourceId</span></span>
<span data-ttu-id="98dfe-134">URI di gestione della risorsa nel sistema esterno.</span><span class="sxs-lookup"><span data-stu-id="98dfe-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="98dfe-135">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="98dfe-135">This parameter is optional.</span></span>
<span data-ttu-id="98dfe-136">Questo URL può essere l'ID delle risorse ARM delle app logiche, delle app funzioni o delle app API.</span><span class="sxs-lookup"><span data-stu-id="98dfe-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="98dfe-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="98dfe-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="98dfe-138">Dettagli del backend del cluster del servizio Fabric.</span><span class="sxs-lookup"><span data-stu-id="98dfe-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="98dfe-139">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="98dfe-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="98dfe-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="98dfe-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="98dfe-141">Se ignorare la convalida della catena di certificati quando si parla con il backend.</span><span class="sxs-lookup"><span data-stu-id="98dfe-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="98dfe-142">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="98dfe-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="98dfe-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="98dfe-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="98dfe-144">Se ignorare la convalida del nome del certificato quando si parla con il backend.</span><span class="sxs-lookup"><span data-stu-id="98dfe-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="98dfe-145">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="98dfe-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="98dfe-146">-Titolo</span><span class="sxs-lookup"><span data-stu-id="98dfe-146">-Title</span></span>
<span data-ttu-id="98dfe-147">Titolo del backend.</span><span class="sxs-lookup"><span data-stu-id="98dfe-147">Backend Title.</span></span>
<span data-ttu-id="98dfe-148">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="98dfe-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="98dfe-149">-URL</span><span class="sxs-lookup"><span data-stu-id="98dfe-149">-Url</span></span>
<span data-ttu-id="98dfe-150">URL di runtime per il backend.</span><span class="sxs-lookup"><span data-stu-id="98dfe-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="98dfe-151">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="98dfe-151">This parameter is required.</span></span>

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

### <span data-ttu-id="98dfe-152">-Confermare</span><span class="sxs-lookup"><span data-stu-id="98dfe-152">-Confirm</span></span>
<span data-ttu-id="98dfe-153">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98dfe-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98dfe-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98dfe-154">-WhatIf</span></span>
<span data-ttu-id="98dfe-155">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98dfe-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98dfe-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98dfe-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98dfe-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98dfe-157">CommonParameters</span></span>
<span data-ttu-id="98dfe-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98dfe-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98dfe-159">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98dfe-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98dfe-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="98dfe-160">INPUTS</span></span>

### <span data-ttu-id="98dfe-161">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="98dfe-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="98dfe-162">System. String</span><span class="sxs-lookup"><span data-stu-id="98dfe-162">System.String</span></span>

### <span data-ttu-id="98dfe-163">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="98dfe-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="98dfe-164">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="98dfe-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="98dfe-165">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="98dfe-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="98dfe-166">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="98dfe-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="98dfe-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98dfe-167">OUTPUTS</span></span>

### <span data-ttu-id="98dfe-168">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="98dfe-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="98dfe-169">Note</span><span class="sxs-lookup"><span data-stu-id="98dfe-169">NOTES</span></span>

## <span data-ttu-id="98dfe-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98dfe-170">RELATED LINKS</span></span>

[<span data-ttu-id="98dfe-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="98dfe-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="98dfe-172">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="98dfe-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="98dfe-173">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="98dfe-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="98dfe-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="98dfe-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="98dfe-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="98dfe-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

