---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
ms.openlocfilehash: d18de5494912900be4a73414e8741badb097d188
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519318"
---
# <span data-ttu-id="1630d-101">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1630d-101">Get-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="1630d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1630d-102">SYNOPSIS</span></span>
<span data-ttu-id="1630d-103">Ottiene tutti o specifici gruppi di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="1630d-103">Gets all or specific API management groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1630d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1630d-104">SYNTAX</span></span>

### <span data-ttu-id="1630d-105">GetAllGroups (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1630d-105">GetAllGroups (Default)</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1630d-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="1630d-106">GetByGroupId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1630d-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="1630d-107">GetByUserId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1630d-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="1630d-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1630d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1630d-109">DESCRIPTION</span></span>
<span data-ttu-id="1630d-110">Il cmdlet **Get-AzureRmApiManagementGroup** ottiene tutti o specifici gruppi di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="1630d-110">The **Get-AzureRmApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="1630d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1630d-111">EXAMPLES</span></span>

### <span data-ttu-id="1630d-112">Esempio 1: ottenere tutti i gruppi</span><span class="sxs-lookup"><span data-stu-id="1630d-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext
```

<span data-ttu-id="1630d-113">Questo comando consente di ottenere tutti i gruppi.</span><span class="sxs-lookup"><span data-stu-id="1630d-113">This command gets all groups.</span></span>

### <span data-ttu-id="1630d-114">Esempio 2: ottenere un gruppo per ID</span><span class="sxs-lookup"><span data-stu-id="1630d-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="1630d-115">Questo comando consente di ottenere l'ID del gruppo denominato 0123456789.</span><span class="sxs-lookup"><span data-stu-id="1630d-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="1630d-116">Esempio 3: ottenere un raggruppamento per nome</span><span class="sxs-lookup"><span data-stu-id="1630d-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="1630d-117">Questo comando ottiene il gruppo denominato Group0002.</span><span class="sxs-lookup"><span data-stu-id="1630d-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="1630d-118">Esempio 4: ottenere tutti i gruppi di utenti</span><span class="sxs-lookup"><span data-stu-id="1630d-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="1630d-119">Questo comando consente di ottenere tutti i gruppi di utenti con l'ID utente denominato 0123456789.</span><span class="sxs-lookup"><span data-stu-id="1630d-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="1630d-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1630d-120">PARAMETERS</span></span>

### <span data-ttu-id="1630d-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="1630d-121">-Context</span></span>
<span data-ttu-id="1630d-122">Specifica un'istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1630d-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="1630d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1630d-123">-DefaultProfile</span></span>
<span data-ttu-id="1630d-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1630d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1630d-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="1630d-125">-GroupId</span></span>
<span data-ttu-id="1630d-126">Specifica l'ID del gruppo.</span><span class="sxs-lookup"><span data-stu-id="1630d-126">Specifies the group ID.</span></span>
<span data-ttu-id="1630d-127">Se specificato, il cmdlet cerca il gruppo in base all'identificatore.</span><span class="sxs-lookup"><span data-stu-id="1630d-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

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

### <span data-ttu-id="1630d-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="1630d-128">-Name</span></span>
<span data-ttu-id="1630d-129">Specifica il nome del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="1630d-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="1630d-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="1630d-130">-ProductId</span></span>
<span data-ttu-id="1630d-131">Identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="1630d-131">Identifier of existing product.</span></span>
<span data-ttu-id="1630d-132">Se specificato restituirà tutti i gruppi a cui è assegnato il prodotto.</span><span class="sxs-lookup"><span data-stu-id="1630d-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="1630d-133">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1630d-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="1630d-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="1630d-134">-UserId</span></span>
<span data-ttu-id="1630d-135">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="1630d-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="1630d-136">Se specificato, il cmdlet restituirà tutti i gruppi a cui viene assegnato il prodotto.</span><span class="sxs-lookup"><span data-stu-id="1630d-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

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

### <span data-ttu-id="1630d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1630d-137">CommonParameters</span></span>
<span data-ttu-id="1630d-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1630d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1630d-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1630d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1630d-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1630d-140">INPUTS</span></span>

### <span data-ttu-id="1630d-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1630d-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1630d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1630d-142">System.String</span></span>

## <span data-ttu-id="1630d-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1630d-143">OUTPUTS</span></span>

### <span data-ttu-id="1630d-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1630d-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="1630d-145">Note</span><span class="sxs-lookup"><span data-stu-id="1630d-145">NOTES</span></span>

## <span data-ttu-id="1630d-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1630d-146">RELATED LINKS</span></span>

[<span data-ttu-id="1630d-147">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1630d-147">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="1630d-148">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1630d-148">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="1630d-149">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1630d-149">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


