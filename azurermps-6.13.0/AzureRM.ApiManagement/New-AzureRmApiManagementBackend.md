---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: 46e0a864bcedd8ac0c23761545f5480eaa4a093a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512044"
---
# <span data-ttu-id="088c7-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="088c7-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="088c7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="088c7-102">SYNOPSIS</span></span>
<span data-ttu-id="088c7-103">Crea una nuova entità back-end.</span><span class="sxs-lookup"><span data-stu-id="088c7-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="088c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="088c7-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="088c7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="088c7-105">DESCRIPTION</span></span>
<span data-ttu-id="088c7-106">Crea una nuova entità back-end nella gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="088c7-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="088c7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="088c7-107">EXAMPLES</span></span>

### <span data-ttu-id="088c7-108">Creare un backend 123 con uno schema di autorizzazione di base</span><span class="sxs-lookup"><span data-stu-id="088c7-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="088c7-109">Crea un nuovo backend</span><span class="sxs-lookup"><span data-stu-id="088c7-109">Creates a new Backend</span></span>

## <span data-ttu-id="088c7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="088c7-110">PARAMETERS</span></span>

### <span data-ttu-id="088c7-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="088c7-111">-BackendId</span></span>
<span data-ttu-id="088c7-112">Identificatore del nuovo backend.</span><span class="sxs-lookup"><span data-stu-id="088c7-112">Identifier of new backend.</span></span>
<span data-ttu-id="088c7-113">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="088c7-113">This parameter is optional.</span></span>
<span data-ttu-id="088c7-114">Se non viene specificato verrà generato.</span><span class="sxs-lookup"><span data-stu-id="088c7-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="088c7-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="088c7-115">-Context</span></span>
<span data-ttu-id="088c7-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="088c7-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="088c7-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="088c7-117">This parameter is required.</span></span>

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

### <span data-ttu-id="088c7-118">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="088c7-118">-Credential</span></span>
<span data-ttu-id="088c7-119">Dettagli delle credenziali che dovrebbero essere usati per comunicare con il backend.</span><span class="sxs-lookup"><span data-stu-id="088c7-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="088c7-120">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="088c7-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="088c7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="088c7-121">-DefaultProfile</span></span>
<span data-ttu-id="088c7-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="088c7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="088c7-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="088c7-123">-Description</span></span>
<span data-ttu-id="088c7-124">Descrizione del backend.</span><span class="sxs-lookup"><span data-stu-id="088c7-124">Backend Description.</span></span>
<span data-ttu-id="088c7-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="088c7-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="088c7-126">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="088c7-126">-Protocol</span></span>
<span data-ttu-id="088c7-127">Protocollo di comunicazione backend.</span><span class="sxs-lookup"><span data-stu-id="088c7-127">Backend Communication protocol.</span></span>
<span data-ttu-id="088c7-128">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="088c7-128">This parameter is required.</span></span>
<span data-ttu-id="088c7-129">I valori validi sono "http" e "SOAP".</span><span class="sxs-lookup"><span data-stu-id="088c7-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="088c7-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="088c7-130">-Proxy</span></span>
<span data-ttu-id="088c7-131">Dettagli del server proxy da usare durante l'invio di una richiesta al backend.</span><span class="sxs-lookup"><span data-stu-id="088c7-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="088c7-132">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="088c7-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="088c7-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="088c7-133">-ResourceId</span></span>
<span data-ttu-id="088c7-134">URI di gestione della risorsa nel sistema esterno.</span><span class="sxs-lookup"><span data-stu-id="088c7-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="088c7-135">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="088c7-135">This parameter is optional.</span></span>
<span data-ttu-id="088c7-136">Questo URL può essere l'ID delle risorse ARM delle app logiche, delle app funzioni o delle app API.</span><span class="sxs-lookup"><span data-stu-id="088c7-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="088c7-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="088c7-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="088c7-138">Dettagli del backend del cluster del servizio Fabric.</span><span class="sxs-lookup"><span data-stu-id="088c7-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="088c7-139">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="088c7-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="088c7-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="088c7-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="088c7-141">Se ignorare la convalida della catena di certificati quando si parla con il backend.</span><span class="sxs-lookup"><span data-stu-id="088c7-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="088c7-142">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="088c7-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="088c7-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="088c7-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="088c7-144">Se ignorare la convalida del nome del certificato quando si parla con il backend.</span><span class="sxs-lookup"><span data-stu-id="088c7-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="088c7-145">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="088c7-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="088c7-146">-Titolo</span><span class="sxs-lookup"><span data-stu-id="088c7-146">-Title</span></span>
<span data-ttu-id="088c7-147">Titolo del backend.</span><span class="sxs-lookup"><span data-stu-id="088c7-147">Backend Title.</span></span>
<span data-ttu-id="088c7-148">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="088c7-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="088c7-149">-URL</span><span class="sxs-lookup"><span data-stu-id="088c7-149">-Url</span></span>
<span data-ttu-id="088c7-150">URL di runtime per il backend.</span><span class="sxs-lookup"><span data-stu-id="088c7-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="088c7-151">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="088c7-151">This parameter is required.</span></span>

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

### <span data-ttu-id="088c7-152">-Confermare</span><span class="sxs-lookup"><span data-stu-id="088c7-152">-Confirm</span></span>
<span data-ttu-id="088c7-153">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="088c7-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="088c7-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="088c7-154">-WhatIf</span></span>
<span data-ttu-id="088c7-155">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="088c7-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="088c7-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="088c7-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="088c7-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="088c7-157">CommonParameters</span></span>
<span data-ttu-id="088c7-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="088c7-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="088c7-159">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="088c7-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="088c7-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="088c7-160">INPUTS</span></span>

### <span data-ttu-id="088c7-161">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="088c7-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="088c7-162">System. String</span><span class="sxs-lookup"><span data-stu-id="088c7-162">System.String</span></span>

### <span data-ttu-id="088c7-163">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="088c7-163">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="088c7-164">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="088c7-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="088c7-165">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="088c7-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="088c7-166">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="088c7-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="088c7-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="088c7-167">OUTPUTS</span></span>

### <span data-ttu-id="088c7-168">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="088c7-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="088c7-169">Note</span><span class="sxs-lookup"><span data-stu-id="088c7-169">NOTES</span></span>

## <span data-ttu-id="088c7-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="088c7-170">RELATED LINKS</span></span>

[<span data-ttu-id="088c7-171">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="088c7-171">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="088c7-172">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="088c7-172">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="088c7-173">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="088c7-173">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="088c7-174">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="088c7-174">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="088c7-175">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="088c7-175">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

