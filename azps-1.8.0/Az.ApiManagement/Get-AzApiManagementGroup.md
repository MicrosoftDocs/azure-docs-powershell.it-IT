---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: a8bef03c7ebe7d20e601ece7c25759f590795ef6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673643"
---
# <span data-ttu-id="84356-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="84356-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="84356-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84356-102">SYNOPSIS</span></span>
<span data-ttu-id="84356-103">Ottiene tutti o specifici gruppi di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="84356-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="84356-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84356-104">SYNTAX</span></span>

### <span data-ttu-id="84356-105">GetAllGroups (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="84356-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84356-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="84356-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84356-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="84356-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84356-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="84356-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84356-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84356-109">DESCRIPTION</span></span>
<span data-ttu-id="84356-110">Il cmdlet **Get-AzApiManagementGroup** ottiene tutti o specifici gruppi di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="84356-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="84356-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84356-111">EXAMPLES</span></span>

### <span data-ttu-id="84356-112">Esempio 1: ottenere tutti i gruppi</span><span class="sxs-lookup"><span data-stu-id="84356-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="84356-113">Questo comando consente di ottenere tutti i gruppi.</span><span class="sxs-lookup"><span data-stu-id="84356-113">This command gets all groups.</span></span>

### <span data-ttu-id="84356-114">Esempio 2: ottenere un gruppo per ID</span><span class="sxs-lookup"><span data-stu-id="84356-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="84356-115">Questo comando consente di ottenere l'ID del gruppo denominato 0123456789.</span><span class="sxs-lookup"><span data-stu-id="84356-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="84356-116">Esempio 3: ottenere un raggruppamento per nome</span><span class="sxs-lookup"><span data-stu-id="84356-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="84356-117">Questo comando ottiene il gruppo denominato Group0002.</span><span class="sxs-lookup"><span data-stu-id="84356-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="84356-118">Esempio 4: ottenere tutti i gruppi di utenti</span><span class="sxs-lookup"><span data-stu-id="84356-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="84356-119">Questo comando consente di ottenere tutti i gruppi di utenti con l'ID utente denominato 0123456789.</span><span class="sxs-lookup"><span data-stu-id="84356-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="84356-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84356-120">PARAMETERS</span></span>

### <span data-ttu-id="84356-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="84356-121">-Context</span></span>
<span data-ttu-id="84356-122">Specifica un'istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="84356-122">Specifies an instance of PsApiManagementContext.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84356-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84356-123">-DefaultProfile</span></span>
<span data-ttu-id="84356-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84356-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84356-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="84356-125">-GroupId</span></span>
<span data-ttu-id="84356-126">Specifica l'ID del gruppo.</span><span class="sxs-lookup"><span data-stu-id="84356-126">Specifies the group ID.</span></span>
<span data-ttu-id="84356-127">Se specificato, il cmdlet cerca il gruppo in base all'identificatore.</span><span class="sxs-lookup"><span data-stu-id="84356-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

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

### <span data-ttu-id="84356-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="84356-128">-Name</span></span>
<span data-ttu-id="84356-129">Specifica il nome del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="84356-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="84356-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="84356-130">-ProductId</span></span>
<span data-ttu-id="84356-131">Identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="84356-131">Identifier of existing product.</span></span>
<span data-ttu-id="84356-132">Se specificato restituirà tutti i gruppi a cui è assegnato il prodotto.</span><span class="sxs-lookup"><span data-stu-id="84356-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="84356-133">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="84356-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="84356-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="84356-134">-UserId</span></span>
<span data-ttu-id="84356-135">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="84356-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="84356-136">Se specificato, il cmdlet restituirà tutti i gruppi a cui viene assegnato il prodotto.</span><span class="sxs-lookup"><span data-stu-id="84356-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

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

### <span data-ttu-id="84356-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84356-137">CommonParameters</span></span>
<span data-ttu-id="84356-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84356-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84356-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84356-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84356-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84356-140">INPUTS</span></span>

### <span data-ttu-id="84356-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="84356-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="84356-142">System. String</span><span class="sxs-lookup"><span data-stu-id="84356-142">System.String</span></span>

## <span data-ttu-id="84356-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84356-143">OUTPUTS</span></span>

### <span data-ttu-id="84356-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="84356-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="84356-145">Note</span><span class="sxs-lookup"><span data-stu-id="84356-145">NOTES</span></span>

## <span data-ttu-id="84356-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84356-146">RELATED LINKS</span></span>

[<span data-ttu-id="84356-147">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="84356-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="84356-148">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="84356-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="84356-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="84356-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


