---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsamplingsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
ms.openlocfilehash: 12f0aa4d198a93d1e392aa61294de6e5815196b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675983"
---
# <span data-ttu-id="fa85c-101">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="fa85c-101">New-AzApiManagementSamplingSetting</span></span>

## <span data-ttu-id="fa85c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fa85c-102">SYNOPSIS</span></span>
<span data-ttu-id="fa85c-103">Creare una nuova impostazione di campionamento per la diagnostica</span><span class="sxs-lookup"><span data-stu-id="fa85c-103">Create a new sampling setting for the Diagnostic</span></span>

## <span data-ttu-id="fa85c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa85c-104">SYNTAX</span></span>

```
New-AzApiManagementSamplingSetting [-SamplingType <String>] [-SamplingPercentage <Double>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa85c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa85c-105">DESCRIPTION</span></span>
<span data-ttu-id="fa85c-106">Il cmdlet **New-AzApiManagementSamplingSetting** crea una nuova impostazione di campionamento per la diagnostica</span><span class="sxs-lookup"><span data-stu-id="fa85c-106">The cmdlet **New-AzApiManagementSamplingSetting** creates a new sampling setting for the Diagnostic</span></span>

## <span data-ttu-id="fa85c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa85c-107">EXAMPLES</span></span>

### <span data-ttu-id="fa85c-108">Esempio 1: creare un'impostazione di campionamento di base</span><span class="sxs-lookup"><span data-stu-id="fa85c-108">Example 1 : Create a basic Sampling setting</span></span>
```powershell
PS C:\> New-AzApiManagementSamplingSetting -SamplingType fixed -Percentage 100

SamplingType Percentage
------------ ----------
fixed               100
```

<span data-ttu-id="fa85c-109">Crea un'impostazione di campionamento di `Fixed` tipo con registrazione per 100% delle richieste/risposte</span><span class="sxs-lookup"><span data-stu-id="fa85c-109">Creates a sampling setting of `Fixed` type with logging for 100% of the requests / responses</span></span>

## <span data-ttu-id="fa85c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fa85c-110">PARAMETERS</span></span>

### <span data-ttu-id="fa85c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa85c-111">-DefaultProfile</span></span>
<span data-ttu-id="fa85c-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fa85c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa85c-113">-SamplingPercentage</span><span class="sxs-lookup"><span data-stu-id="fa85c-113">-SamplingPercentage</span></span>
<span data-ttu-id="fa85c-114">Tasso di campionamento per il campionamento a tasso fisso.</span><span class="sxs-lookup"><span data-stu-id="fa85c-114">Rate of Sampling for Fixed Rate Sampling.</span></span> <span data-ttu-id="fa85c-115">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fa85c-115">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa85c-116">-SamplingType</span><span class="sxs-lookup"><span data-stu-id="fa85c-116">-SamplingType</span></span>
<span data-ttu-id="fa85c-117">Tipo di campionamento.</span><span class="sxs-lookup"><span data-stu-id="fa85c-117">The Type of Sampling.</span></span>
<span data-ttu-id="fa85c-118">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fa85c-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa85c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa85c-119">CommonParameters</span></span>
<span data-ttu-id="fa85c-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa85c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa85c-121">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa85c-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa85c-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fa85c-122">INPUTS</span></span>

### <span data-ttu-id="fa85c-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fa85c-123">None</span></span>

## <span data-ttu-id="fa85c-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa85c-124">OUTPUTS</span></span>

### <span data-ttu-id="fa85c-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="fa85c-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

## <span data-ttu-id="fa85c-126">Note</span><span class="sxs-lookup"><span data-stu-id="fa85c-126">NOTES</span></span>

## <span data-ttu-id="fa85c-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa85c-127">RELATED LINKS</span></span>

[<span data-ttu-id="fa85c-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="fa85c-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="fa85c-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="fa85c-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="fa85c-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="fa85c-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="fa85c-131">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="fa85c-131">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)