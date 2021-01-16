---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: 10c84654bb5d074ee9f668062d1fa7a18d92f8b0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356495"
---
# <span data-ttu-id="847e7-101">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="847e7-101">New-AzApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="847e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="847e7-102">SYNOPSIS</span></span>
<span data-ttu-id="847e7-103">Crea un'istanza di **PsApiManagementHttpMessageDiagnostic** che è un'impostazione di diagnostica del messaggio http della diagnostica</span><span class="sxs-lookup"><span data-stu-id="847e7-103">Creates an instance of **PsApiManagementHttpMessageDiagnostic** which is an Http Message diagnostic setting of the Diagnostic</span></span>

## <span data-ttu-id="847e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="847e7-104">SYNTAX</span></span>

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="847e7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="847e7-105">DESCRIPTION</span></span>
<span data-ttu-id="847e7-106">Il cmdlet **New-AzApiManagementHttpMessageDiagnostic** crea l'impostazione di diagnostica del messaggio http.</span><span class="sxs-lookup"><span data-stu-id="847e7-106">The cmdlet **New-AzApiManagementHttpMessageDiagnostic** creates the Http Message diagnostic setting.</span></span>

## <span data-ttu-id="847e7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="847e7-107">EXAMPLES</span></span>

### <span data-ttu-id="847e7-108">Esempio 1: creare un'impostazione di diagnostica messaggio http di base</span><span class="sxs-lookup"><span data-stu-id="847e7-108">Example 1: Create a Basic Http Message diagnostic Setting</span></span>
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

<span data-ttu-id="847e7-109">Creare un'impostazione di diagnostica per i messaggi HTTP per registrare `Content-Type` e `User-Agent` intestazioni insieme a 100 byte di `body`</span><span class="sxs-lookup"><span data-stu-id="847e7-109">Create a http message diagnostic setting to log `Content-Type` and `User-Agent` headers along with 100 bytes of `body`</span></span>

## <span data-ttu-id="847e7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="847e7-110">PARAMETERS</span></span>

### <span data-ttu-id="847e7-111">-BodyBytesToLog</span><span class="sxs-lookup"><span data-stu-id="847e7-111">-BodyBytesToLog</span></span>
<span data-ttu-id="847e7-112">Numero di byte del corpo della richiesta da registrare.</span><span class="sxs-lookup"><span data-stu-id="847e7-112">Number of request body bytes to log.</span></span> <span data-ttu-id="847e7-113">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="847e7-113">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="847e7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="847e7-114">-DefaultProfile</span></span>
<span data-ttu-id="847e7-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="847e7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="847e7-116">-HeadersToLog</span><span class="sxs-lookup"><span data-stu-id="847e7-116">-HeadersToLog</span></span>
<span data-ttu-id="847e7-117">Matrice di intestazioni da registrare.</span><span class="sxs-lookup"><span data-stu-id="847e7-117">The array of headers to log.</span></span> <span data-ttu-id="847e7-118">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="847e7-118">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="847e7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="847e7-119">CommonParameters</span></span>
<span data-ttu-id="847e7-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="847e7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="847e7-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="847e7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="847e7-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="847e7-122">INPUTS</span></span>

### <span data-ttu-id="847e7-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="847e7-123">None</span></span>

## <span data-ttu-id="847e7-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="847e7-124">OUTPUTS</span></span>

### <span data-ttu-id="847e7-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="847e7-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="847e7-126">Note</span><span class="sxs-lookup"><span data-stu-id="847e7-126">NOTES</span></span>

## <span data-ttu-id="847e7-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="847e7-127">RELATED LINKS</span></span>

[<span data-ttu-id="847e7-128">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="847e7-128">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="847e7-129">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="847e7-129">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)