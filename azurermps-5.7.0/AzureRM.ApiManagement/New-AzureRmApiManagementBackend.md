---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: c337e82c88c7fdbbc1f8a3663249126c9d92b19f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521481"
---
# <span data-ttu-id="8a79e-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8a79e-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="8a79e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a79e-102">SYNOPSIS</span></span>
<span data-ttu-id="8a79e-103">Crea una nuova entità back-end.</span><span class="sxs-lookup"><span data-stu-id="8a79e-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a79e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a79e-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a79e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a79e-105">DESCRIPTION</span></span>
<span data-ttu-id="8a79e-106">Crea una nuova entità back-end nella gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="8a79e-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="8a79e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a79e-107">EXAMPLES</span></span>

### <span data-ttu-id="8a79e-108">Creare un backend 123 con uno schema di autorizzazione di base</span><span class="sxs-lookup"><span data-stu-id="8a79e-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="8a79e-109">Crea un nuovo backend</span><span class="sxs-lookup"><span data-stu-id="8a79e-109">Creates a new Backend</span></span>

## <span data-ttu-id="8a79e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a79e-110">PARAMETERS</span></span>

### <span data-ttu-id="8a79e-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="8a79e-111">-BackendId</span></span>
<span data-ttu-id="8a79e-112">Identificatore del nuovo backend.</span><span class="sxs-lookup"><span data-stu-id="8a79e-112">Identifier of new backend.</span></span>
<span data-ttu-id="8a79e-113">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8a79e-113">This parameter is optional.</span></span>
<span data-ttu-id="8a79e-114">Se non viene specificato verrà generato.</span><span class="sxs-lookup"><span data-stu-id="8a79e-114">If not specified will be generated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a79e-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="8a79e-115">-Context</span></span>
<span data-ttu-id="8a79e-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8a79e-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8a79e-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8a79e-117">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a79e-118">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="8a79e-118">-Credential</span></span>
<span data-ttu-id="8a79e-119">Dettagli delle credenziali che dovrebbero essere usati per comunicare con il backend.</span><span class="sxs-lookup"><span data-stu-id="8a79e-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="8a79e-120">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8a79e-120">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementBackendCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a79e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a79e-121">-DefaultProfile</span></span>
<span data-ttu-id="8a79e-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8a79e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a79e-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a79e-123">-Description</span></span>
<span data-ttu-id="8a79e-124">Descrizione del backend.</span><span class="sxs-lookup"><span data-stu-id="8a79e-124">Backend Description.</span></span>
<span data-ttu-id="8a79e-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8a79e-125">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a79e-126">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="8a79e-126">-Protocol</span></span>
<span data-ttu-id="8a79e-127">Protocollo di comunicazione backend.</span><span class="sxs-lookup"><span data-stu-id="8a79e-127">Backend Communication protocol.</span></span>
<span data-ttu-id="8a79e-128">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8a79e-128">This parameter is required.</span></span>
<span data-ttu-id="8a79e-129">I valori validi sono "http" e "SOAP".</span><span class="sxs-lookup"><span data-stu-id="8a79e-129">Valid values are 'http' and 'soap'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a79e-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="8a79e-130">-Proxy</span></span>
<span data-ttu-id="8a79e-131">Dettagli del server proxy da usare durante l'invio di una richiesta al backend.</span><span class="sxs-lookup"><span data-stu-id="8a79e-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="8a79e-132">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8a79e-132">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a79e-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a79e-133">-ResourceId</span></span>
<span data-ttu-id="8a79e-134">URI di gestione della risorsa nel sistema esterno.</span><span class="sxs-lookup"><span data-stu-id="8a79e-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="8a79e-135">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8a79e-135">This parameter is optional.</span></span>
<span data-ttu-id="8a79e-136">Questo URL può essere l'ID delle risorse ARM delle app logiche, delle app funzioni o delle app API.</span><span class="sxs-lookup"><span data-stu-id="8a79e-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a79e-137">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="8a79e-137">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="8a79e-138">Se ignorare la convalida della catena di certificati quando si parla con il backend.</span><span class="sxs-lookup"><span data-stu-id="8a79e-138">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="8a79e-139">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8a79e-139">This parameter is optional.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a79e-140">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="8a79e-140">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="8a79e-141">Se ignorare la convalida del nome del certificato quando si parla con il backend.</span><span class="sxs-lookup"><span data-stu-id="8a79e-141">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="8a79e-142">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8a79e-142">This parameter is optional.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a79e-143">-Titolo</span><span class="sxs-lookup"><span data-stu-id="8a79e-143">-Title</span></span>
<span data-ttu-id="8a79e-144">Titolo del backend.</span><span class="sxs-lookup"><span data-stu-id="8a79e-144">Backend Title.</span></span>
<span data-ttu-id="8a79e-145">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8a79e-145">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a79e-146">-URL</span><span class="sxs-lookup"><span data-stu-id="8a79e-146">-Url</span></span>
<span data-ttu-id="8a79e-147">URL di runtime per il backend.</span><span class="sxs-lookup"><span data-stu-id="8a79e-147">Runtime Url for the Backend.</span></span>
<span data-ttu-id="8a79e-148">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8a79e-148">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a79e-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8a79e-149">-Confirm</span></span>
<span data-ttu-id="8a79e-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a79e-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a79e-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a79e-151">-WhatIf</span></span>
<span data-ttu-id="8a79e-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a79e-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a79e-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a79e-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a79e-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a79e-154">CommonParameters</span></span>
<span data-ttu-id="8a79e-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a79e-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a79e-156">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a79e-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a79e-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a79e-157">INPUTS</span></span>

### <span data-ttu-id="8a79e-158">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8a79e-158">None</span></span>
<span data-ttu-id="8a79e-159">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="8a79e-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8a79e-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a79e-160">OUTPUTS</span></span>

### <span data-ttu-id="8a79e-161">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8a79e-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="8a79e-162">Note</span><span class="sxs-lookup"><span data-stu-id="8a79e-162">NOTES</span></span>

## <span data-ttu-id="8a79e-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a79e-163">RELATED LINKS</span></span>

[<span data-ttu-id="8a79e-164">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8a79e-164">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="8a79e-165">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="8a79e-165">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="8a79e-166">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="8a79e-166">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="8a79e-167">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8a79e-167">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="8a79e-168">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8a79e-168">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

