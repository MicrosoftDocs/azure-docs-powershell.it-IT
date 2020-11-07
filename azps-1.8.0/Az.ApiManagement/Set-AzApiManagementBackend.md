---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: ce27a151ebb6d778ed647fb81909c44c11edbf8e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852393"
---
# <span data-ttu-id="12670-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="12670-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="12670-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12670-102">SYNOPSIS</span></span>
<span data-ttu-id="12670-103">Aggiorna un backend.</span><span class="sxs-lookup"><span data-stu-id="12670-103">Updates a Backend.</span></span>

## <span data-ttu-id="12670-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12670-104">SYNTAX</span></span>

```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12670-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12670-105">DESCRIPTION</span></span>
<span data-ttu-id="12670-106">Aggiorna un backend esistente nella gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="12670-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="12670-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12670-107">EXAMPLES</span></span>

### <span data-ttu-id="12670-108">Aggiorna la descrizione del backend 123</span><span class="sxs-lookup"><span data-stu-id="12670-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="12670-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12670-109">PARAMETERS</span></span>

### <span data-ttu-id="12670-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="12670-110">-BackendId</span></span>
<span data-ttu-id="12670-111">Identificatore del nuovo backend.</span><span class="sxs-lookup"><span data-stu-id="12670-111">Identifier of new backend.</span></span>
<span data-ttu-id="12670-112">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="12670-112">This parameter is required.</span></span>

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

### <span data-ttu-id="12670-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="12670-113">-Context</span></span>
<span data-ttu-id="12670-114">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="12670-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="12670-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="12670-115">This parameter is required.</span></span>

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

### <span data-ttu-id="12670-116">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="12670-116">-Credential</span></span>
<span data-ttu-id="12670-117">Dettagli delle credenziali che dovrebbero essere usati per comunicare con il backend.</span><span class="sxs-lookup"><span data-stu-id="12670-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="12670-118">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="12670-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="12670-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12670-119">-DefaultProfile</span></span>
<span data-ttu-id="12670-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12670-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12670-121">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="12670-121">-Description</span></span>
<span data-ttu-id="12670-122">Descrizione del backend.</span><span class="sxs-lookup"><span data-stu-id="12670-122">Backend Description.</span></span>
<span data-ttu-id="12670-123">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="12670-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="12670-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12670-124">-PassThru</span></span>
<span data-ttu-id="12670-125">Indica che questo cmdlet restituisce il  **PsApiManagementBackend** modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12670-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="12670-126">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="12670-126">-Protocol</span></span>
<span data-ttu-id="12670-127">Protocollo di comunicazione backend (http o SOAP).</span><span class="sxs-lookup"><span data-stu-id="12670-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="12670-128">Questo parametro è facoltativo</span><span class="sxs-lookup"><span data-stu-id="12670-128">This parameter is optional</span></span>

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

### <span data-ttu-id="12670-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="12670-129">-Proxy</span></span>
<span data-ttu-id="12670-130">Dettagli del server proxy da usare durante l'invio di una richiesta al backend.</span><span class="sxs-lookup"><span data-stu-id="12670-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="12670-131">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="12670-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="12670-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12670-132">-ResourceId</span></span>
<span data-ttu-id="12670-133">URI di gestione della risorsa nel sistema esterno.</span><span class="sxs-lookup"><span data-stu-id="12670-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="12670-134">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="12670-134">This parameter is optional.</span></span>
<span data-ttu-id="12670-135">Questo URL può essere l'ID delle risorse ARM delle app logiche, delle app funzioni o delle app API.</span><span class="sxs-lookup"><span data-stu-id="12670-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="12670-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="12670-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="12670-137">Dettagli del backend del cluster del servizio Fabric.</span><span class="sxs-lookup"><span data-stu-id="12670-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="12670-138">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="12670-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="12670-139">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="12670-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="12670-140">Se ignorare la convalida della catena di certificati quando si parla con il backend.</span><span class="sxs-lookup"><span data-stu-id="12670-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="12670-141">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="12670-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="12670-142">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="12670-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="12670-143">Se ignorare la convalida del nome del certificato quando si parla con il backend.</span><span class="sxs-lookup"><span data-stu-id="12670-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="12670-144">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="12670-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="12670-145">-Titolo</span><span class="sxs-lookup"><span data-stu-id="12670-145">-Title</span></span>
<span data-ttu-id="12670-146">Titolo del backend.</span><span class="sxs-lookup"><span data-stu-id="12670-146">Backend Title.</span></span>
<span data-ttu-id="12670-147">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="12670-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="12670-148">-URL</span><span class="sxs-lookup"><span data-stu-id="12670-148">-Url</span></span>
<span data-ttu-id="12670-149">URL di runtime per il backend.</span><span class="sxs-lookup"><span data-stu-id="12670-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="12670-150">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="12670-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="12670-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="12670-151">-Confirm</span></span>
<span data-ttu-id="12670-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12670-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12670-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12670-153">-WhatIf</span></span>
<span data-ttu-id="12670-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12670-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12670-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12670-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12670-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12670-156">CommonParameters</span></span>
<span data-ttu-id="12670-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12670-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12670-158">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12670-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12670-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12670-159">INPUTS</span></span>

### <span data-ttu-id="12670-160">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="12670-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="12670-161">System. String</span><span class="sxs-lookup"><span data-stu-id="12670-161">System.String</span></span>

### <span data-ttu-id="12670-162">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="12670-162">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="12670-163">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="12670-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="12670-164">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="12670-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="12670-165">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="12670-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="12670-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="12670-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="12670-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12670-167">OUTPUTS</span></span>

### <span data-ttu-id="12670-168">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="12670-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="12670-169">Note</span><span class="sxs-lookup"><span data-stu-id="12670-169">NOTES</span></span>

## <span data-ttu-id="12670-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12670-170">RELATED LINKS</span></span>

[<span data-ttu-id="12670-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="12670-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="12670-172">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="12670-172">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="12670-173">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="12670-173">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="12670-174">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="12670-174">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="12670-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="12670-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
