---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
ms.openlocfilehash: 2867e8eec65de040a0da61a1af960abc9797bb18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686874"
---
# <span data-ttu-id="ee887-101">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="ee887-101">Remove-AzureRmApiManagementUserFromGroup</span></span>

## <span data-ttu-id="ee887-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee887-102">SYNOPSIS</span></span>
<span data-ttu-id="ee887-103">Rimuove un utente da un gruppo.</span><span class="sxs-lookup"><span data-stu-id="ee887-103">Removes a user from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee887-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee887-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee887-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee887-105">DESCRIPTION</span></span>
<span data-ttu-id="ee887-106">Il cmdlet **Remove-AzureRmApiManagementUserFromGroup** rimuove un utente da un gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="ee887-106">The **Remove-AzureRmApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="ee887-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee887-107">EXAMPLES</span></span>

### <span data-ttu-id="ee887-108">Esempio 1: rimuovere un utente da un gruppo</span><span class="sxs-lookup"><span data-stu-id="ee887-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>Remove-AzureRmApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="ee887-109">Questo comando rimuove un utente da un gruppo.</span><span class="sxs-lookup"><span data-stu-id="ee887-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="ee887-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee887-110">PARAMETERS</span></span>

### <span data-ttu-id="ee887-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="ee887-111">-Context</span></span>
<span data-ttu-id="ee887-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ee887-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="ee887-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ee887-113">This parameter is required.</span></span>

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

### <span data-ttu-id="ee887-114">-GroupId</span><span class="sxs-lookup"><span data-stu-id="ee887-114">-GroupId</span></span>
<span data-ttu-id="ee887-115">Specifica l'ID del gruppo da cui rimuovere un utente.</span><span class="sxs-lookup"><span data-stu-id="ee887-115">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="ee887-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee887-116">-PassThru</span></span>
<span data-ttu-id="ee887-117">Indica che questo cmdlet restituisce un valore di $True, se ha esito positivo o un valore di $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ee887-117">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="ee887-118">-UserId</span><span class="sxs-lookup"><span data-stu-id="ee887-118">-UserId</span></span>
<span data-ttu-id="ee887-119">Specifica l'ID dell'utente da rimuovere dal gruppo.</span><span class="sxs-lookup"><span data-stu-id="ee887-119">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="ee887-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee887-120">-DefaultProfile</span></span>
<span data-ttu-id="ee887-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ee887-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee887-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee887-122">CommonParameters</span></span>
<span data-ttu-id="ee887-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee887-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee887-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee887-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee887-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee887-125">INPUTS</span></span>

## <span data-ttu-id="ee887-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee887-126">OUTPUTS</span></span>

### <span data-ttu-id="ee887-127">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ee887-127">System.Boolean</span></span>

## <span data-ttu-id="ee887-128">Note</span><span class="sxs-lookup"><span data-stu-id="ee887-128">NOTES</span></span>

## <span data-ttu-id="ee887-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee887-129">RELATED LINKS</span></span>

[<span data-ttu-id="ee887-130">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="ee887-130">Add-AzureRmApiManagementUserToGroup</span></span>](./Add-AzureRmApiManagementUserToGroup.md)

[<span data-ttu-id="ee887-131">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ee887-131">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


