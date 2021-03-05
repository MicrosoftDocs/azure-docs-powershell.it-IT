---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementpipelinediagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
ms.openlocfilehash: e68449a84bb64454291434bded40ed2e494fdab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979053"
---
# <span data-ttu-id="8752b-101">New-AzApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="8752b-101">New-AzApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="8752b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8752b-102">SYNOPSIS</span></span>
<span data-ttu-id="8752b-103">Creare impostazioni di diagnostica per i messaggi HTTP in arrivo/in uscita al gateway.</span><span class="sxs-lookup"><span data-stu-id="8752b-103">Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="8752b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8752b-104">SYNTAX</span></span>

```
New-AzApiManagementPipelineDiagnosticSetting [-Request <PsApiManagementHttpMessageDiagnostic>]
 [-Response <PsApiManagementHttpMessageDiagnostic>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8752b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8752b-105">DESCRIPTION</span></span>
<span data-ttu-id="8752b-106">Il cmdlet **New-AzApiManagementPipelineDiagnosticSetting** crea le impostazioni di diagnostica per i messaggi HTTP in ingresso/in uscita nel gateway.</span><span class="sxs-lookup"><span data-stu-id="8752b-106">The cmdlet **New-AzApiManagementPipelineDiagnosticSetting** creates the Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="8752b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8752b-107">EXAMPLES</span></span>

### <span data-ttu-id="8752b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8752b-108">Example 1</span></span>
```powershell
PS c:\> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100
PS c:\> New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic

Request                                                                                              Response
-------                                                                                              --------
Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
```

<span data-ttu-id="8752b-109">Creare una diagnostica della pipeline da usare in FrontEnd o Back-end nell'entità di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="8752b-109">Create a pipeline diagnostic to be used in either FrontEnd or Backend in the Diagnostic Entity.</span></span>

## <span data-ttu-id="8752b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8752b-110">PARAMETERS</span></span>

### <span data-ttu-id="8752b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8752b-111">-DefaultProfile</span></span>
<span data-ttu-id="8752b-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8752b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8752b-113">-Request</span><span class="sxs-lookup"><span data-stu-id="8752b-113">-Request</span></span>
<span data-ttu-id="8752b-114">Impostazione diagnostica per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="8752b-114">Diagnostic setting for Request.</span></span>
<span data-ttu-id="8752b-115">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8752b-115">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8752b-116">-Response</span><span class="sxs-lookup"><span data-stu-id="8752b-116">-Response</span></span>
<span data-ttu-id="8752b-117">Impostazione diagnostica per la risposta.</span><span class="sxs-lookup"><span data-stu-id="8752b-117">Diagnostic setting for Response.</span></span>
<span data-ttu-id="8752b-118">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8752b-118">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8752b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8752b-119">CommonParameters</span></span>
<span data-ttu-id="8752b-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8752b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8752b-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8752b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8752b-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="8752b-122">INPUTS</span></span>

### <span data-ttu-id="8752b-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8752b-123">None</span></span>

## <span data-ttu-id="8752b-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8752b-124">OUTPUTS</span></span>

### <span data-ttu-id="8752b-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="8752b-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="8752b-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="8752b-126">NOTES</span></span>

## <span data-ttu-id="8752b-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8752b-127">RELATED LINKS</span></span>

[<span data-ttu-id="8752b-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8752b-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="8752b-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8752b-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="8752b-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8752b-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="8752b-131">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8752b-131">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)


