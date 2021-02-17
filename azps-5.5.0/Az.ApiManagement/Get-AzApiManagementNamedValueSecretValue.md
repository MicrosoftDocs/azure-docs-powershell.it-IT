---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvaluesecretvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
ms.openlocfilehash: 5ec602e4cd86086a7be8e7ae53c1c2bb551a963c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205730"
---
# <span data-ttu-id="c79fc-101">Get-AzApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="c79fc-101">Get-AzApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="c79fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c79fc-102">SYNOPSIS</span></span>
<span data-ttu-id="c79fc-103">Ottiene un valore segreto del valore denominato specifico.</span><span class="sxs-lookup"><span data-stu-id="c79fc-103">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="c79fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c79fc-104">SYNTAX</span></span>

### <span data-ttu-id="c79fc-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c79fc-105">Default (Default)</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c79fc-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="c79fc-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext> -NamedValueId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c79fc-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c79fc-107">DESCRIPTION</span></span>
<span data-ttu-id="c79fc-108">Ottiene un valore segreto del valore denominato specifico.</span><span class="sxs-lookup"><span data-stu-id="c79fc-108">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="c79fc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c79fc-109">EXAMPLES</span></span>

### <span data-ttu-id="c79fc-110">Esempio 1: Ottenere un valore denominato in base al nome</span><span class="sxs-lookup"><span data-stu-id="c79fc-110">Example 1: Get named value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValueSecretValue -Context $apimContext -NamedValueId "sql-connectionstring"
```

<span data-ttu-id="c79fc-111">Questo comando recupera i dettagli del valore denominato in base al nome del valore denominato.</span><span class="sxs-lookup"><span data-stu-id="c79fc-111">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="c79fc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c79fc-112">PARAMETERS</span></span>

### <span data-ttu-id="c79fc-113">-Context</span><span class="sxs-lookup"><span data-stu-id="c79fc-113">-Context</span></span>
<span data-ttu-id="c79fc-114">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c79fc-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c79fc-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c79fc-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c79fc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c79fc-116">-DefaultProfile</span></span>
<span data-ttu-id="c79fc-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c79fc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c79fc-118">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="c79fc-118">-NamedValueId</span></span>
<span data-ttu-id="c79fc-119">Identificatore di un valore denominato.</span><span class="sxs-lookup"><span data-stu-id="c79fc-119">Identifier of a the named value.</span></span>
<span data-ttu-id="c79fc-120">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c79fc-120">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c79fc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c79fc-121">CommonParameters</span></span>
<span data-ttu-id="c79fc-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c79fc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c79fc-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c79fc-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c79fc-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="c79fc-124">INPUTS</span></span>

### <span data-ttu-id="c79fc-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c79fc-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c79fc-126">System.String</span><span class="sxs-lookup"><span data-stu-id="c79fc-126">System.String</span></span>

## <span data-ttu-id="c79fc-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c79fc-127">OUTPUTS</span></span>

### <span data-ttu-id="c79fc-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="c79fc-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="c79fc-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="c79fc-129">NOTES</span></span>

## <span data-ttu-id="c79fc-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c79fc-130">RELATED LINKS</span></span>
