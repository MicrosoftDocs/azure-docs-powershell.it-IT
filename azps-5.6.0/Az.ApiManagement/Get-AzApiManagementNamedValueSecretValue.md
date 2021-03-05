---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementnamedvaluesecretvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
ms.openlocfilehash: 1ef17239338319696d08a316648a158039fa63f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975613"
---
# <span data-ttu-id="6105a-101">Get-AzApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="6105a-101">Get-AzApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="6105a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6105a-102">SYNOPSIS</span></span>
<span data-ttu-id="6105a-103">Ottiene un valore segreto del valore denominato specifico.</span><span class="sxs-lookup"><span data-stu-id="6105a-103">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="6105a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6105a-104">SYNTAX</span></span>

### <span data-ttu-id="6105a-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6105a-105">Default (Default)</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6105a-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="6105a-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext> -NamedValueId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6105a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6105a-107">DESCRIPTION</span></span>
<span data-ttu-id="6105a-108">Ottiene un valore segreto del valore denominato specifico.</span><span class="sxs-lookup"><span data-stu-id="6105a-108">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="6105a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6105a-109">EXAMPLES</span></span>

### <span data-ttu-id="6105a-110">Esempio 1: Ottenere un valore denominato in base al nome</span><span class="sxs-lookup"><span data-stu-id="6105a-110">Example 1: Get named value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValueSecretValue -Context $apimContext -NamedValueId "sql-connectionstring"
```

<span data-ttu-id="6105a-111">Questo comando recupera i dettagli del valore denominato a cui viene assegnato il nome del valore denominato.</span><span class="sxs-lookup"><span data-stu-id="6105a-111">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="6105a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6105a-112">PARAMETERS</span></span>

### <span data-ttu-id="6105a-113">-Context</span><span class="sxs-lookup"><span data-stu-id="6105a-113">-Context</span></span>
<span data-ttu-id="6105a-114">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6105a-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6105a-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="6105a-115">This parameter is required.</span></span>

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

### <span data-ttu-id="6105a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6105a-116">-DefaultProfile</span></span>
<span data-ttu-id="6105a-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6105a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6105a-118">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="6105a-118">-NamedValueId</span></span>
<span data-ttu-id="6105a-119">Identificatore di un valore denominato.</span><span class="sxs-lookup"><span data-stu-id="6105a-119">Identifier of a the named value.</span></span>
<span data-ttu-id="6105a-120">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="6105a-120">This parameter is required.</span></span>

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

### <span data-ttu-id="6105a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6105a-121">CommonParameters</span></span>
<span data-ttu-id="6105a-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6105a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6105a-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6105a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6105a-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="6105a-124">INPUTS</span></span>

### <span data-ttu-id="6105a-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6105a-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6105a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="6105a-126">System.String</span></span>

## <span data-ttu-id="6105a-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6105a-127">OUTPUTS</span></span>

### <span data-ttu-id="6105a-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="6105a-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="6105a-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="6105a-129">NOTES</span></span>

## <span data-ttu-id="6105a-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6105a-130">RELATED LINKS</span></span>
