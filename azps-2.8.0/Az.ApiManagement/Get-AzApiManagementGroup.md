---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: 9a8acd17f953e90cd5b4311854830da03dc4df0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676071"
---
# <span data-ttu-id="d7793-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d7793-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="d7793-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d7793-102">SYNOPSIS</span></span>
<span data-ttu-id="d7793-103">Ottiene tutti o specifici gruppi di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="d7793-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="d7793-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7793-104">SYNTAX</span></span>

### <span data-ttu-id="d7793-105">GetAllGroups (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d7793-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7793-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="d7793-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7793-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="d7793-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7793-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="d7793-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7793-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7793-109">DESCRIPTION</span></span>
<span data-ttu-id="d7793-110">Il cmdlet **Get-AzApiManagementGroup** ottiene tutti o specifici gruppi di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="d7793-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="d7793-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7793-111">EXAMPLES</span></span>

### <span data-ttu-id="d7793-112">Esempio 1: ottenere tutti i gruppi</span><span class="sxs-lookup"><span data-stu-id="d7793-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="d7793-113">Questo comando consente di ottenere tutti i gruppi.</span><span class="sxs-lookup"><span data-stu-id="d7793-113">This command gets all groups.</span></span>

### <span data-ttu-id="d7793-114">Esempio 2: ottenere un gruppo per ID</span><span class="sxs-lookup"><span data-stu-id="d7793-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="d7793-115">Questo comando consente di ottenere l'ID del gruppo denominato 0123456789.</span><span class="sxs-lookup"><span data-stu-id="d7793-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="d7793-116">Esempio 3: ottenere un raggruppamento per nome</span><span class="sxs-lookup"><span data-stu-id="d7793-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="d7793-117">Questo comando ottiene il gruppo denominato Group0002.</span><span class="sxs-lookup"><span data-stu-id="d7793-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="d7793-118">Esempio 4: ottenere tutti i gruppi di utenti</span><span class="sxs-lookup"><span data-stu-id="d7793-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="d7793-119">Questo comando consente di ottenere tutti i gruppi di utenti con l'ID utente denominato 0123456789.</span><span class="sxs-lookup"><span data-stu-id="d7793-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="d7793-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d7793-120">PARAMETERS</span></span>

### <span data-ttu-id="d7793-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="d7793-121">-Context</span></span>
<span data-ttu-id="d7793-122">Specifica un'istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d7793-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="d7793-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7793-123">-DefaultProfile</span></span>
<span data-ttu-id="d7793-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d7793-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7793-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="d7793-125">-GroupId</span></span>
<span data-ttu-id="d7793-126">Specifica l'ID del gruppo.</span><span class="sxs-lookup"><span data-stu-id="d7793-126">Specifies the group ID.</span></span>
<span data-ttu-id="d7793-127">Se specificato, il cmdlet cerca il gruppo in base all'identificatore.</span><span class="sxs-lookup"><span data-stu-id="d7793-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

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

### <span data-ttu-id="d7793-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7793-128">-Name</span></span>
<span data-ttu-id="d7793-129">Specifica il nome del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="d7793-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="d7793-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="d7793-130">-ProductId</span></span>
<span data-ttu-id="d7793-131">Identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="d7793-131">Identifier of existing product.</span></span>
<span data-ttu-id="d7793-132">Se specificato restituirà tutti i gruppi a cui è assegnato il prodotto.</span><span class="sxs-lookup"><span data-stu-id="d7793-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="d7793-133">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d7793-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="d7793-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="d7793-134">-UserId</span></span>
<span data-ttu-id="d7793-135">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="d7793-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="d7793-136">Se specificato, il cmdlet restituirà tutti i gruppi a cui viene assegnato il prodotto.</span><span class="sxs-lookup"><span data-stu-id="d7793-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

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

### <span data-ttu-id="d7793-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7793-137">CommonParameters</span></span>
<span data-ttu-id="d7793-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7793-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7793-139">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7793-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7793-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d7793-140">INPUTS</span></span>

### <span data-ttu-id="d7793-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d7793-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d7793-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d7793-142">System.String</span></span>

## <span data-ttu-id="d7793-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7793-143">OUTPUTS</span></span>

### <span data-ttu-id="d7793-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d7793-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="d7793-145">Note</span><span class="sxs-lookup"><span data-stu-id="d7793-145">NOTES</span></span>

## <span data-ttu-id="d7793-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7793-146">RELATED LINKS</span></span>

[<span data-ttu-id="d7793-147">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d7793-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="d7793-148">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d7793-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="d7793-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d7793-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


