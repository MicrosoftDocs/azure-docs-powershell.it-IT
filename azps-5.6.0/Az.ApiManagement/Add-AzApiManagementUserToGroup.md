---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/add-azapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
ms.openlocfilehash: a56acc56bc100365f999ef1ca9a5f42f53b36096
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994628"
---
# <span data-ttu-id="13e9c-101">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="13e9c-101">Add-AzApiManagementUserToGroup</span></span>

## <span data-ttu-id="13e9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13e9c-102">SYNOPSIS</span></span>
<span data-ttu-id="13e9c-103">Aggiunge un utente a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="13e9c-103">Adds a user to a group.</span></span>

## <span data-ttu-id="13e9c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13e9c-104">SYNTAX</span></span>

```
Add-AzApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13e9c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="13e9c-105">DESCRIPTION</span></span>
<span data-ttu-id="13e9c-106">Il cmdlet **Add-AzApiManagementUserToGroup** aggiunge un utente a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="13e9c-106">The **Add-AzApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="13e9c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13e9c-107">EXAMPLES</span></span>

### <span data-ttu-id="13e9c-108">Esempio 1: Aggiungere un utente a un gruppo</span><span class="sxs-lookup"><span data-stu-id="13e9c-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="13e9c-109">Questo comando aggiunge un utente esistente a un gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="13e9c-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="13e9c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13e9c-110">PARAMETERS</span></span>

### <span data-ttu-id="13e9c-111">-Context</span><span class="sxs-lookup"><span data-stu-id="13e9c-111">-Context</span></span>
<span data-ttu-id="13e9c-112">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="13e9c-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="13e9c-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="13e9c-113">This parameter is required.</span></span>

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

### <span data-ttu-id="13e9c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13e9c-114">-DefaultProfile</span></span>
<span data-ttu-id="13e9c-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="13e9c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13e9c-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="13e9c-116">-GroupId</span></span>
<span data-ttu-id="13e9c-117">Specifica l'ID gruppo.</span><span class="sxs-lookup"><span data-stu-id="13e9c-117">Specifies the group ID.</span></span>
<span data-ttu-id="13e9c-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="13e9c-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13e9c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13e9c-119">-PassThru</span></span>
<span data-ttu-id="13e9c-120">passthru</span><span class="sxs-lookup"><span data-stu-id="13e9c-120">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13e9c-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="13e9c-121">-UserId</span></span>
<span data-ttu-id="13e9c-122">Specifica l'ID utente.</span><span class="sxs-lookup"><span data-stu-id="13e9c-122">Specifies the user ID.</span></span>
<span data-ttu-id="13e9c-123">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="13e9c-123">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13e9c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13e9c-124">CommonParameters</span></span>
<span data-ttu-id="13e9c-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13e9c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13e9c-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="13e9c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13e9c-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="13e9c-127">INPUTS</span></span>

### <span data-ttu-id="13e9c-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="13e9c-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="13e9c-129">System.String</span><span class="sxs-lookup"><span data-stu-id="13e9c-129">System.String</span></span>

### <span data-ttu-id="13e9c-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="13e9c-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="13e9c-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13e9c-131">OUTPUTS</span></span>

### <span data-ttu-id="13e9c-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="13e9c-132">System.Boolean</span></span>

## <span data-ttu-id="13e9c-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="13e9c-133">NOTES</span></span>

## <span data-ttu-id="13e9c-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13e9c-134">RELATED LINKS</span></span>

[<span data-ttu-id="13e9c-135">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="13e9c-135">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="13e9c-136">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="13e9c-136">Remove-AzApiManagementUserFromGroup</span></span>](./Remove-AzApiManagementUserFromGroup.md)


