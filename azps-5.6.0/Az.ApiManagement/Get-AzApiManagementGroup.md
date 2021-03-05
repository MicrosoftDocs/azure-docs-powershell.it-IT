---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: 786d095b7750843688b4319eec7e46263332a4c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960926"
---
# <span data-ttu-id="49cf9-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="49cf9-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="49cf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="49cf9-103">Recupera tutti i gruppi di gestione delle API o specifici.</span><span class="sxs-lookup"><span data-stu-id="49cf9-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="49cf9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49cf9-104">SYNTAX</span></span>

### <span data-ttu-id="49cf9-105">GetAllGroups (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="49cf9-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49cf9-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="49cf9-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49cf9-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="49cf9-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49cf9-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="49cf9-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49cf9-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="49cf9-109">DESCRIPTION</span></span>
<span data-ttu-id="49cf9-110">Il **cmdlet Get-AzApiManagementGroup** ottiene tutti i gruppi di gestione delle API o solo uno specifico.</span><span class="sxs-lookup"><span data-stu-id="49cf9-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="49cf9-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49cf9-111">EXAMPLES</span></span>

### <span data-ttu-id="49cf9-112">Esempio 1: Ottenere tutti i gruppi</span><span class="sxs-lookup"><span data-stu-id="49cf9-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="49cf9-113">Questo comando recupera tutti i gruppi.</span><span class="sxs-lookup"><span data-stu-id="49cf9-113">This command gets all groups.</span></span>

### <span data-ttu-id="49cf9-114">Esempio 2: Ottenere un gruppo in base all'ID</span><span class="sxs-lookup"><span data-stu-id="49cf9-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="49cf9-115">Questo comando ottiene l'ID gruppo denominato 0123456789.</span><span class="sxs-lookup"><span data-stu-id="49cf9-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="49cf9-116">Esempio 3: Ottenere un gruppo in base al nome</span><span class="sxs-lookup"><span data-stu-id="49cf9-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="49cf9-117">Questo comando recupera il gruppo denominato Gruppo0002.</span><span class="sxs-lookup"><span data-stu-id="49cf9-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="49cf9-118">Esempio 4: Ottenere tutti i gruppi di utenti</span><span class="sxs-lookup"><span data-stu-id="49cf9-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="49cf9-119">Questo comando recupera tutti i gruppi di utenti il cui ID utente è denominato 0123456789.</span><span class="sxs-lookup"><span data-stu-id="49cf9-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="49cf9-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49cf9-120">PARAMETERS</span></span>

### <span data-ttu-id="49cf9-121">-Context</span><span class="sxs-lookup"><span data-stu-id="49cf9-121">-Context</span></span>
<span data-ttu-id="49cf9-122">Specifica un'istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="49cf9-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="49cf9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49cf9-123">-DefaultProfile</span></span>
<span data-ttu-id="49cf9-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49cf9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49cf9-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="49cf9-125">-GroupId</span></span>
<span data-ttu-id="49cf9-126">Specifica l'ID gruppo.</span><span class="sxs-lookup"><span data-stu-id="49cf9-126">Specifies the group ID.</span></span>
<span data-ttu-id="49cf9-127">Se specificato, il cmdlet prova a trovare il gruppo in base all'identificatore.</span><span class="sxs-lookup"><span data-stu-id="49cf9-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGroupId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49cf9-128">-Name</span><span class="sxs-lookup"><span data-stu-id="49cf9-128">-Name</span></span>
<span data-ttu-id="49cf9-129">Specifica il nome del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="49cf9-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="49cf9-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="49cf9-130">-ProductId</span></span>
<span data-ttu-id="49cf9-131">Identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="49cf9-131">Identifier of existing product.</span></span>
<span data-ttu-id="49cf9-132">Se specificato restituirà tutti i gruppi a cui è assegnato il prodotto.</span><span class="sxs-lookup"><span data-stu-id="49cf9-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="49cf9-133">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="49cf9-133">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49cf9-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="49cf9-134">-UserId</span></span>
<span data-ttu-id="49cf9-135">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="49cf9-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="49cf9-136">Se specificato, il cmdlet restituirà tutti i gruppi a cui è assegnato il prodotto.</span><span class="sxs-lookup"><span data-stu-id="49cf9-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49cf9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49cf9-137">CommonParameters</span></span>
<span data-ttu-id="49cf9-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49cf9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49cf9-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="49cf9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49cf9-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="49cf9-140">INPUTS</span></span>

### <span data-ttu-id="49cf9-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="49cf9-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="49cf9-142">System.String</span><span class="sxs-lookup"><span data-stu-id="49cf9-142">System.String</span></span>

## <span data-ttu-id="49cf9-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49cf9-143">OUTPUTS</span></span>

### <span data-ttu-id="49cf9-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="49cf9-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="49cf9-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="49cf9-145">NOTES</span></span>

## <span data-ttu-id="49cf9-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49cf9-146">RELATED LINKS</span></span>

[<span data-ttu-id="49cf9-147">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="49cf9-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="49cf9-148">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="49cf9-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="49cf9-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="49cf9-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


