---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
ms.openlocfilehash: 27e6be451d6141e322c47b2a84a28baf115839ef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187775"
---
# <span data-ttu-id="39d7e-101">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="39d7e-101">Add-AzApiManagementUserToGroup</span></span>

## <span data-ttu-id="39d7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39d7e-102">SYNOPSIS</span></span>
<span data-ttu-id="39d7e-103">Aggiunge un utente a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="39d7e-103">Adds a user to a group.</span></span>

## <span data-ttu-id="39d7e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39d7e-104">SYNTAX</span></span>

```
Add-AzApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39d7e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="39d7e-105">DESCRIPTION</span></span>
<span data-ttu-id="39d7e-106">Il cmdlet **Add-AzApiManagementUserToGroup** aggiunge un utente a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="39d7e-106">The **Add-AzApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="39d7e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39d7e-107">EXAMPLES</span></span>

### <span data-ttu-id="39d7e-108">Esempio 1: Aggiungere un utente a un gruppo</span><span class="sxs-lookup"><span data-stu-id="39d7e-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="39d7e-109">Questo comando aggiunge un utente esistente a un gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="39d7e-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="39d7e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39d7e-110">PARAMETERS</span></span>

### <span data-ttu-id="39d7e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="39d7e-111">-Context</span></span>
<span data-ttu-id="39d7e-112">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="39d7e-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="39d7e-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="39d7e-113">This parameter is required.</span></span>

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

### <span data-ttu-id="39d7e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39d7e-114">-DefaultProfile</span></span>
<span data-ttu-id="39d7e-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39d7e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39d7e-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="39d7e-116">-GroupId</span></span>
<span data-ttu-id="39d7e-117">Specifica l'ID gruppo.</span><span class="sxs-lookup"><span data-stu-id="39d7e-117">Specifies the group ID.</span></span>
<span data-ttu-id="39d7e-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="39d7e-118">This parameter is required.</span></span>

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

### <span data-ttu-id="39d7e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39d7e-119">-PassThru</span></span>
<span data-ttu-id="39d7e-120">passthru</span><span class="sxs-lookup"><span data-stu-id="39d7e-120">passthru</span></span>

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

### <span data-ttu-id="39d7e-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="39d7e-121">-UserId</span></span>
<span data-ttu-id="39d7e-122">Specifica l'ID utente.</span><span class="sxs-lookup"><span data-stu-id="39d7e-122">Specifies the user ID.</span></span>
<span data-ttu-id="39d7e-123">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="39d7e-123">This parameter is required.</span></span>

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

### <span data-ttu-id="39d7e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39d7e-124">CommonParameters</span></span>
<span data-ttu-id="39d7e-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39d7e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39d7e-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="39d7e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39d7e-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="39d7e-127">INPUTS</span></span>

### <span data-ttu-id="39d7e-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="39d7e-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="39d7e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="39d7e-129">System.String</span></span>

### <span data-ttu-id="39d7e-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="39d7e-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="39d7e-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39d7e-131">OUTPUTS</span></span>

### <span data-ttu-id="39d7e-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="39d7e-132">System.Boolean</span></span>

## <span data-ttu-id="39d7e-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="39d7e-133">NOTES</span></span>

## <span data-ttu-id="39d7e-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39d7e-134">RELATED LINKS</span></span>

[<span data-ttu-id="39d7e-135">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="39d7e-135">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="39d7e-136">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="39d7e-136">Remove-AzApiManagementUserFromGroup</span></span>](./Remove-AzApiManagementUserFromGroup.md)


