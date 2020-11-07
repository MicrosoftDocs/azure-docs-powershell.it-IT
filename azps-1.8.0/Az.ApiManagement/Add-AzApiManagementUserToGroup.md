---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
ms.openlocfilehash: 2d33ece97d2a0ef007b5970afef499fbb6f2117e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673667"
---
# <span data-ttu-id="f0c99-101">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="f0c99-101">Add-AzApiManagementUserToGroup</span></span>

## <span data-ttu-id="f0c99-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f0c99-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c99-103">Aggiunge un utente a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="f0c99-103">Adds a user to a group.</span></span>

## <span data-ttu-id="f0c99-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0c99-104">SYNTAX</span></span>

```
Add-AzApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0c99-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0c99-105">DESCRIPTION</span></span>
<span data-ttu-id="f0c99-106">Il cmdlet **Add-AzApiManagementUserToGroup** aggiunge un utente a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="f0c99-106">The **Add-AzApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="f0c99-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0c99-107">EXAMPLES</span></span>

### <span data-ttu-id="f0c99-108">Esempio 1: aggiungere un utente a un gruppo</span><span class="sxs-lookup"><span data-stu-id="f0c99-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="f0c99-109">Questo comando aggiunge un utente esistente a un gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="f0c99-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="f0c99-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f0c99-110">PARAMETERS</span></span>

### <span data-ttu-id="f0c99-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="f0c99-111">-Context</span></span>
<span data-ttu-id="f0c99-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f0c99-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f0c99-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f0c99-113">This parameter is required.</span></span>

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

### <span data-ttu-id="f0c99-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0c99-114">-DefaultProfile</span></span>
<span data-ttu-id="f0c99-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f0c99-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0c99-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="f0c99-116">-GroupId</span></span>
<span data-ttu-id="f0c99-117">Specifica l'ID del gruppo.</span><span class="sxs-lookup"><span data-stu-id="f0c99-117">Specifies the group ID.</span></span>
<span data-ttu-id="f0c99-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f0c99-118">This parameter is required.</span></span>

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

### <span data-ttu-id="f0c99-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0c99-119">-PassThru</span></span>
<span data-ttu-id="f0c99-120">PassThru</span><span class="sxs-lookup"><span data-stu-id="f0c99-120">passthru</span></span>

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

### <span data-ttu-id="f0c99-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="f0c99-121">-UserId</span></span>
<span data-ttu-id="f0c99-122">Specifica l'ID utente.</span><span class="sxs-lookup"><span data-stu-id="f0c99-122">Specifies the user ID.</span></span>
<span data-ttu-id="f0c99-123">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f0c99-123">This parameter is required.</span></span>

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

### <span data-ttu-id="f0c99-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c99-124">CommonParameters</span></span>
<span data-ttu-id="f0c99-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0c99-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c99-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0c99-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c99-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f0c99-127">INPUTS</span></span>

### <span data-ttu-id="f0c99-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f0c99-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f0c99-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f0c99-129">System.String</span></span>

### <span data-ttu-id="f0c99-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f0c99-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f0c99-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0c99-131">OUTPUTS</span></span>

### <span data-ttu-id="f0c99-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f0c99-132">System.Boolean</span></span>

## <span data-ttu-id="f0c99-133">Note</span><span class="sxs-lookup"><span data-stu-id="f0c99-133">NOTES</span></span>

## <span data-ttu-id="f0c99-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0c99-134">RELATED LINKS</span></span>

[<span data-ttu-id="f0c99-135">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f0c99-135">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="f0c99-136">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="f0c99-136">Remove-AzApiManagementUserFromGroup</span></span>](./Remove-AzApiManagementUserFromGroup.md)


