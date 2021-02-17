---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: c7f88f204bbb6d4999e6ddb1f0f3e2942500daf7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205763"
---
# <span data-ttu-id="9171f-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9171f-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="9171f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9171f-102">SYNOPSIS</span></span>
<span data-ttu-id="9171f-103">Recupera tutti i gruppi di gestione delle API o specifici.</span><span class="sxs-lookup"><span data-stu-id="9171f-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="9171f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9171f-104">SYNTAX</span></span>

### <span data-ttu-id="9171f-105">GetAllGroups (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9171f-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9171f-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="9171f-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9171f-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="9171f-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9171f-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="9171f-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9171f-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9171f-109">DESCRIPTION</span></span>
<span data-ttu-id="9171f-110">Il **cmdlet Get-AzApiManagementGroup** ottiene tutti i gruppi di gestione delle API o solo uno specifico.</span><span class="sxs-lookup"><span data-stu-id="9171f-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="9171f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9171f-111">EXAMPLES</span></span>

### <span data-ttu-id="9171f-112">Esempio 1: Ottenere tutti i gruppi</span><span class="sxs-lookup"><span data-stu-id="9171f-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="9171f-113">Questo comando recupera tutti i gruppi.</span><span class="sxs-lookup"><span data-stu-id="9171f-113">This command gets all groups.</span></span>

### <span data-ttu-id="9171f-114">Esempio 2: Ottenere un gruppo in base all'ID</span><span class="sxs-lookup"><span data-stu-id="9171f-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="9171f-115">Questo comando ottiene l'ID gruppo denominato 0123456789.</span><span class="sxs-lookup"><span data-stu-id="9171f-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="9171f-116">Esempio 3: Ottenere un gruppo in base al nome</span><span class="sxs-lookup"><span data-stu-id="9171f-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="9171f-117">Questo comando recupera il gruppo denominato Gruppo0002.</span><span class="sxs-lookup"><span data-stu-id="9171f-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="9171f-118">Esempio 4: Ottenere tutti i gruppi di utenti</span><span class="sxs-lookup"><span data-stu-id="9171f-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="9171f-119">Questo comando recupera tutti i gruppi di utenti il cui ID utente è denominato 0123456789.</span><span class="sxs-lookup"><span data-stu-id="9171f-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="9171f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9171f-120">PARAMETERS</span></span>

### <span data-ttu-id="9171f-121">-Context</span><span class="sxs-lookup"><span data-stu-id="9171f-121">-Context</span></span>
<span data-ttu-id="9171f-122">Specifica un'istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9171f-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="9171f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9171f-123">-DefaultProfile</span></span>
<span data-ttu-id="9171f-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9171f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9171f-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="9171f-125">-GroupId</span></span>
<span data-ttu-id="9171f-126">Specifica l'ID gruppo.</span><span class="sxs-lookup"><span data-stu-id="9171f-126">Specifies the group ID.</span></span>
<span data-ttu-id="9171f-127">Se specificato, il cmdlet prova a trovare il gruppo in base all'identificatore.</span><span class="sxs-lookup"><span data-stu-id="9171f-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

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

### <span data-ttu-id="9171f-128">-Name</span><span class="sxs-lookup"><span data-stu-id="9171f-128">-Name</span></span>
<span data-ttu-id="9171f-129">Specifica il nome del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="9171f-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="9171f-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="9171f-130">-ProductId</span></span>
<span data-ttu-id="9171f-131">Identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="9171f-131">Identifier of existing product.</span></span>
<span data-ttu-id="9171f-132">Se specificato restituirà tutti i gruppi a cui è assegnato il prodotto.</span><span class="sxs-lookup"><span data-stu-id="9171f-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="9171f-133">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9171f-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="9171f-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="9171f-134">-UserId</span></span>
<span data-ttu-id="9171f-135">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="9171f-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="9171f-136">Se specificato, il cmdlet restituirà tutti i gruppi a cui è assegnato il prodotto.</span><span class="sxs-lookup"><span data-stu-id="9171f-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

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

### <span data-ttu-id="9171f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9171f-137">CommonParameters</span></span>
<span data-ttu-id="9171f-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9171f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9171f-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9171f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9171f-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="9171f-140">INPUTS</span></span>

### <span data-ttu-id="9171f-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9171f-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9171f-142">System.String</span><span class="sxs-lookup"><span data-stu-id="9171f-142">System.String</span></span>

## <span data-ttu-id="9171f-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9171f-143">OUTPUTS</span></span>

### <span data-ttu-id="9171f-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9171f-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="9171f-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="9171f-145">NOTES</span></span>

## <span data-ttu-id="9171f-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9171f-146">RELATED LINKS</span></span>

[<span data-ttu-id="9171f-147">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9171f-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="9171f-148">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9171f-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="9171f-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9171f-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


