---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 9826de76a65fe097d2daba106bd74df5e94a730e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205802"
---
# <span data-ttu-id="5fcb3-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="5fcb3-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="5fcb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fcb3-102">SYNOPSIS</span></span>
<span data-ttu-id="5fcb3-103">Recupera i certificati di gestione DELLE API configurati per l'autenticazione reciproca con Back-end nel servizio.</span><span class="sxs-lookup"><span data-stu-id="5fcb3-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="5fcb3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5fcb3-104">SYNTAX</span></span>

### <span data-ttu-id="5fcb3-105">ContextParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5fcb3-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fcb3-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fcb3-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCertificate [-CertificateId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fcb3-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5fcb3-107">DESCRIPTION</span></span>
<span data-ttu-id="5fcb3-108">Il **cmdlet Get-AzApiManagementCertificate** ottiene tutti i certificati o i certificati di Gestione API di Azure specificati.</span><span class="sxs-lookup"><span data-stu-id="5fcb3-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="5fcb3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5fcb3-109">EXAMPLES</span></span>

### <span data-ttu-id="5fcb3-110">Esempio 1: Ottenere tutti i certificati</span><span class="sxs-lookup"><span data-stu-id="5fcb3-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="5fcb3-111">Questo comando recupera tutti i certificati di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="5fcb3-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="5fcb3-112">Esempio 2: Ottenere un certificato in base al relativo ID</span><span class="sxs-lookup"><span data-stu-id="5fcb3-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="5fcb3-113">Questo comando ottiene il certificato di gestione API con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="5fcb3-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="5fcb3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fcb3-114">PARAMETERS</span></span>

### <span data-ttu-id="5fcb3-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="5fcb3-115">-CertificateId</span></span>
<span data-ttu-id="5fcb3-116">Specifica l'ID del certificato da ottenere.</span><span class="sxs-lookup"><span data-stu-id="5fcb3-116">Specifies the ID of the certificate to get.</span></span>

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

### <span data-ttu-id="5fcb3-117">-Context</span><span class="sxs-lookup"><span data-stu-id="5fcb3-117">-Context</span></span>
<span data-ttu-id="5fcb3-118">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="5fcb3-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5fcb3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fcb3-119">-DefaultProfile</span></span>
<span data-ttu-id="5fcb3-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5fcb3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fcb3-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fcb3-121">-ResourceId</span></span>
<span data-ttu-id="5fcb3-122">Arm Resource Identifier of the Certificate.</span><span class="sxs-lookup"><span data-stu-id="5fcb3-122">Arm Resource Identifier of the Certificate.</span></span> <span data-ttu-id="5fcb3-123">Se specificato, tenterà di trovare il certificato in base all'identificatore.</span><span class="sxs-lookup"><span data-stu-id="5fcb3-123">If specified will try to find certificate by the identifier.</span></span> <span data-ttu-id="5fcb3-124">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5fcb3-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fcb3-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5fcb3-125">-Confirm</span></span>
<span data-ttu-id="5fcb3-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fcb3-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fcb3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fcb3-127">-WhatIf</span></span>
<span data-ttu-id="5fcb3-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5fcb3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fcb3-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5fcb3-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fcb3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fcb3-130">CommonParameters</span></span>
<span data-ttu-id="5fcb3-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fcb3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fcb3-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5fcb3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fcb3-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="5fcb3-133">INPUTS</span></span>

### <span data-ttu-id="5fcb3-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5fcb3-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5fcb3-135">System.String</span><span class="sxs-lookup"><span data-stu-id="5fcb3-135">System.String</span></span>

## <span data-ttu-id="5fcb3-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5fcb3-136">OUTPUTS</span></span>

### <span data-ttu-id="5fcb3-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="5fcb3-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="5fcb3-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="5fcb3-138">NOTES</span></span>

## <span data-ttu-id="5fcb3-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5fcb3-139">RELATED LINKS</span></span>

[<span data-ttu-id="5fcb3-140">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="5fcb3-140">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="5fcb3-141">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="5fcb3-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="5fcb3-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="5fcb3-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


