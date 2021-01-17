---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: c7f88f204bbb6d4999e6ddb1f0f3e2942500daf7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478959"
---
# <span data-ttu-id="d2576-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d2576-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="d2576-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2576-102">SYNOPSIS</span></span>
<span data-ttu-id="d2576-103">Ottiene tutti o specifici gruppi di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="d2576-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="d2576-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2576-104">SYNTAX</span></span>

### <span data-ttu-id="d2576-105">GetAllGroups (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d2576-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2576-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="d2576-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2576-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="d2576-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2576-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="d2576-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2576-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2576-109">DESCRIPTION</span></span>
<span data-ttu-id="d2576-110">Il cmdlet **Get-AzApiManagementGroup** ottiene tutti o specifici gruppi di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="d2576-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="d2576-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2576-111">EXAMPLES</span></span>

### <span data-ttu-id="d2576-112">Esempio 1: ottenere tutti i gruppi</span><span class="sxs-lookup"><span data-stu-id="d2576-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="d2576-113">Questo comando consente di ottenere tutti i gruppi.</span><span class="sxs-lookup"><span data-stu-id="d2576-113">This command gets all groups.</span></span>

### <span data-ttu-id="d2576-114">Esempio 2: ottenere un gruppo per ID</span><span class="sxs-lookup"><span data-stu-id="d2576-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="d2576-115">Questo comando consente di ottenere l'ID del gruppo denominato 0123456789.</span><span class="sxs-lookup"><span data-stu-id="d2576-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="d2576-116">Esempio 3: ottenere un raggruppamento per nome</span><span class="sxs-lookup"><span data-stu-id="d2576-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="d2576-117">Questo comando ottiene il gruppo denominato Group0002.</span><span class="sxs-lookup"><span data-stu-id="d2576-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="d2576-118">Esempio 4: ottenere tutti i gruppi di utenti</span><span class="sxs-lookup"><span data-stu-id="d2576-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="d2576-119">Questo comando consente di ottenere tutti i gruppi di utenti con l'ID utente denominato 0123456789.</span><span class="sxs-lookup"><span data-stu-id="d2576-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="d2576-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2576-120">PARAMETERS</span></span>

### <span data-ttu-id="d2576-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="d2576-121">-Context</span></span>
<span data-ttu-id="d2576-122">Specifica un'istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d2576-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="d2576-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2576-123">-DefaultProfile</span></span>
<span data-ttu-id="d2576-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d2576-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2576-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="d2576-125">-GroupId</span></span>
<span data-ttu-id="d2576-126">Specifica l'ID del gruppo.</span><span class="sxs-lookup"><span data-stu-id="d2576-126">Specifies the group ID.</span></span>
<span data-ttu-id="d2576-127">Se specificato, il cmdlet cerca il gruppo in base all'identificatore.</span><span class="sxs-lookup"><span data-stu-id="d2576-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

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

### <span data-ttu-id="d2576-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2576-128">-Name</span></span>
<span data-ttu-id="d2576-129">Specifica il nome del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="d2576-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="d2576-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="d2576-130">-ProductId</span></span>
<span data-ttu-id="d2576-131">Identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="d2576-131">Identifier of existing product.</span></span>
<span data-ttu-id="d2576-132">Se specificato restituirà tutti i gruppi a cui è assegnato il prodotto.</span><span class="sxs-lookup"><span data-stu-id="d2576-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="d2576-133">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d2576-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="d2576-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="d2576-134">-UserId</span></span>
<span data-ttu-id="d2576-135">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="d2576-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="d2576-136">Se specificato, il cmdlet restituirà tutti i gruppi a cui viene assegnato il prodotto.</span><span class="sxs-lookup"><span data-stu-id="d2576-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

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

### <span data-ttu-id="d2576-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2576-137">CommonParameters</span></span>
<span data-ttu-id="d2576-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2576-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2576-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2576-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2576-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2576-140">INPUTS</span></span>

### <span data-ttu-id="d2576-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d2576-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d2576-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d2576-142">System.String</span></span>

## <span data-ttu-id="d2576-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2576-143">OUTPUTS</span></span>

### <span data-ttu-id="d2576-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d2576-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="d2576-145">Note</span><span class="sxs-lookup"><span data-stu-id="d2576-145">NOTES</span></span>

## <span data-ttu-id="d2576-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2576-146">RELATED LINKS</span></span>

[<span data-ttu-id="d2576-147">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d2576-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="d2576-148">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d2576-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="d2576-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d2576-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


