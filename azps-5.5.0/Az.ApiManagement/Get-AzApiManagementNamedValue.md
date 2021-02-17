---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
ms.openlocfilehash: 8d6d7174278d1f997c6a62e75eec4958f75b1d6c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205738"
---
# <span data-ttu-id="b727f-101">Get-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="b727f-101">Get-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="b727f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b727f-102">SYNOPSIS</span></span>
<span data-ttu-id="b727f-103">Ottiene un elenco o un determinato valore denominato.</span><span class="sxs-lookup"><span data-stu-id="b727f-103">Gets a list or a particular Named Value.</span></span>

## <span data-ttu-id="b727f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b727f-104">SYNTAX</span></span>

### <span data-ttu-id="b727f-105">GetAllNamedValues (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b727f-105">GetAllNamedValues (Default)</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b727f-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="b727f-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b727f-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="b727f-107">GetByName</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b727f-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="b727f-108">GetByTag</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b727f-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b727f-109">DESCRIPTION</span></span>
<span data-ttu-id="b727f-110">Il **cmdlet Get-AzApiManagementNamedValue** ottiene un elenco o un determinato valore denominato.</span><span class="sxs-lookup"><span data-stu-id="b727f-110">The **Get-AzApiManagementNamedValue** cmdlet gets a list or a particular named value.</span></span>
<span data-ttu-id="b727f-111">Il valore non verrà incluso nei dettagli del risultato se il valore denominato è contrassegnato come segreto.</span><span class="sxs-lookup"><span data-stu-id="b727f-111">Value will not be included into result details if the named value marked as a secret.</span></span> <span data-ttu-id="b727f-112">Per ottenere un valore segreto, usare **Get-AzApiManagementNamedValueSecretValue.**</span><span class="sxs-lookup"><span data-stu-id="b727f-112">To get secret value, use **Get-AzApiManagementNamedValueSecretValue**.</span></span>

## <span data-ttu-id="b727f-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b727f-113">EXAMPLES</span></span>

### <span data-ttu-id="b727f-114">Esempio 1: Ottenere un valore denominato in base al nome</span><span class="sxs-lookup"><span data-stu-id="b727f-114">Example 1: Get Named Value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValue -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="b727f-115">Questo comando recupera i dettagli del valore denominato in base al nome del valore denominato.</span><span class="sxs-lookup"><span data-stu-id="b727f-115">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="b727f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b727f-116">PARAMETERS</span></span>

### <span data-ttu-id="b727f-117">-Context</span><span class="sxs-lookup"><span data-stu-id="b727f-117">-Context</span></span>
<span data-ttu-id="b727f-118">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b727f-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b727f-119">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b727f-119">This parameter is required.</span></span>

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

### <span data-ttu-id="b727f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b727f-120">-DefaultProfile</span></span>
<span data-ttu-id="b727f-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b727f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b727f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b727f-122">-Name</span></span>
<span data-ttu-id="b727f-123">Trova valori denominati con nomi contenenti il nome della stringa.</span><span class="sxs-lookup"><span data-stu-id="b727f-123">Finds named values with names containing the string Name.</span></span>
<span data-ttu-id="b727f-124">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b727f-124">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b727f-125">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="b727f-125">-NamedValueId</span></span>
<span data-ttu-id="b727f-126">Identificatore del valore denominato.</span><span class="sxs-lookup"><span data-stu-id="b727f-126">Identifier of the named value.</span></span>
<span data-ttu-id="b727f-127">Se specificato, tenterà di trovare un valore denominato in base all'identificatore.</span><span class="sxs-lookup"><span data-stu-id="b727f-127">If specified will try to find named value by the identifier.</span></span>
<span data-ttu-id="b727f-128">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b727f-128">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b727f-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="b727f-129">-Tag</span></span>
<span data-ttu-id="b727f-130">Trova i valori denominati associati a un tag.</span><span class="sxs-lookup"><span data-stu-id="b727f-130">Finds named values associated with a Tag.</span></span>
<span data-ttu-id="b727f-131">Se specificato restituirà tutte le proprietà associate a un tag.</span><span class="sxs-lookup"><span data-stu-id="b727f-131">If specified will return all properties associated with a tag.</span></span>
<span data-ttu-id="b727f-132">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b727f-132">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTag
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b727f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b727f-133">CommonParameters</span></span>
<span data-ttu-id="b727f-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b727f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b727f-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b727f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b727f-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="b727f-136">INPUTS</span></span>

### <span data-ttu-id="b727f-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b727f-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b727f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b727f-138">System.String</span></span>

## <span data-ttu-id="b727f-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b727f-139">OUTPUTS</span></span>

### <span data-ttu-id="b727f-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="b727f-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="b727f-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="b727f-141">NOTES</span></span>

## <span data-ttu-id="b727f-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b727f-142">RELATED LINKS</span></span>
