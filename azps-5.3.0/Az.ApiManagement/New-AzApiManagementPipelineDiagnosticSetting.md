---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementpipelinediagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
ms.openlocfilehash: 7e6f6515b24a7cefabd40a6fdfaedfda430f69d0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382437"
---
# <span data-ttu-id="ec825-101">New-AzApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="ec825-101">New-AzApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="ec825-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ec825-102">SYNOPSIS</span></span>
<span data-ttu-id="ec825-103">Creare impostazioni di diagnostica per i messaggi HTTP in arrivo/in uscita nel gateway.</span><span class="sxs-lookup"><span data-stu-id="ec825-103">Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="ec825-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec825-104">SYNTAX</span></span>

```
New-AzApiManagementPipelineDiagnosticSetting [-Request <PsApiManagementHttpMessageDiagnostic>]
 [-Response <PsApiManagementHttpMessageDiagnostic>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec825-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec825-105">DESCRIPTION</span></span>
<span data-ttu-id="ec825-106">Il cmdlet **New-AzApiManagementPipelineDiagnosticSetting** crea le impostazioni di diagnostica per i messaggi HTTP in arrivo/in uscita nel gateway.</span><span class="sxs-lookup"><span data-stu-id="ec825-106">The cmdlet **New-AzApiManagementPipelineDiagnosticSetting** creates the Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="ec825-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec825-107">EXAMPLES</span></span>

### <span data-ttu-id="ec825-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ec825-108">Example 1</span></span>
```powershell
PS c:\> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100
PS c:\> New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic

Request                                                                                              Response
-------                                                                                              --------
Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
```

<span data-ttu-id="ec825-109">Creare un sistema di diagnostica della pipeline da usare in FrontEnd o backend nell'entità di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="ec825-109">Create a pipeline diagnostic to be used in either FrontEnd or Backend in the Diagnostic Entity.</span></span>

## <span data-ttu-id="ec825-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec825-110">PARAMETERS</span></span>

### <span data-ttu-id="ec825-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec825-111">-DefaultProfile</span></span>
<span data-ttu-id="ec825-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ec825-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec825-113">-Request</span><span class="sxs-lookup"><span data-stu-id="ec825-113">-Request</span></span>
<span data-ttu-id="ec825-114">Impostazione di diagnostica per Request.</span><span class="sxs-lookup"><span data-stu-id="ec825-114">Diagnostic setting for Request.</span></span>
<span data-ttu-id="ec825-115">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ec825-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="ec825-116">-Risposta</span><span class="sxs-lookup"><span data-stu-id="ec825-116">-Response</span></span>
<span data-ttu-id="ec825-117">Impostazione di diagnostica per la risposta.</span><span class="sxs-lookup"><span data-stu-id="ec825-117">Diagnostic setting for Response.</span></span>
<span data-ttu-id="ec825-118">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ec825-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="ec825-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec825-119">CommonParameters</span></span>
<span data-ttu-id="ec825-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec825-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec825-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec825-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec825-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ec825-122">INPUTS</span></span>

### <span data-ttu-id="ec825-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ec825-123">None</span></span>

## <span data-ttu-id="ec825-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec825-124">OUTPUTS</span></span>

### <span data-ttu-id="ec825-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="ec825-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="ec825-126">Note</span><span class="sxs-lookup"><span data-stu-id="ec825-126">NOTES</span></span>

## <span data-ttu-id="ec825-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec825-127">RELATED LINKS</span></span>

[<span data-ttu-id="ec825-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ec825-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="ec825-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ec825-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="ec825-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ec825-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="ec825-131">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ec825-131">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)


