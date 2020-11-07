---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
ms.openlocfilehash: b0f4e67630a3a762fe78c9438c6ae39f948404c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687708"
---
# <span data-ttu-id="30d8a-101">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="30d8a-101">Remove-AzureRmADUser</span></span>

## <span data-ttu-id="30d8a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30d8a-102">SYNOPSIS</span></span>
<span data-ttu-id="30d8a-103">Elimina un utente di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="30d8a-103">Deletes an active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30d8a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30d8a-104">SYNTAX</span></span>

```
Remove-AzureRmADUser -UPNOrObjectId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30d8a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30d8a-105">DESCRIPTION</span></span>
<span data-ttu-id="30d8a-106">Elimina un utente di Active Directory (account aziendale o dell'Istituto di istruzione noto anche come org-ID).</span><span class="sxs-lookup"><span data-stu-id="30d8a-106">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="30d8a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30d8a-107">EXAMPLES</span></span>

### <span data-ttu-id="30d8a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="30d8a-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="30d8a-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="30d8a-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="30d8a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30d8a-110">PARAMETERS</span></span>

### <span data-ttu-id="30d8a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="30d8a-111">-Force</span></span>
<span data-ttu-id="30d8a-112">Se specificato, non chiede conferma per l'eliminazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="30d8a-112">If specified, doesn't ask for confirmation for deleting user.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d8a-113">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="30d8a-113">-UPNOrObjectId</span></span>
<span data-ttu-id="30d8a-114">Nome dell'entità utente o objectId dell'utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="30d8a-114">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="30d8a-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="30d8a-115">-Confirm</span></span>
<span data-ttu-id="30d8a-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30d8a-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d8a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30d8a-117">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d8a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30d8a-118">-DefaultProfile</span></span>
<span data-ttu-id="30d8a-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="30d8a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30d8a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30d8a-120">CommonParameters</span></span>
<span data-ttu-id="30d8a-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30d8a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30d8a-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30d8a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30d8a-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30d8a-123">INPUTS</span></span>

## <span data-ttu-id="30d8a-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30d8a-124">OUTPUTS</span></span>

## <span data-ttu-id="30d8a-125">Note</span><span class="sxs-lookup"><span data-stu-id="30d8a-125">NOTES</span></span>

## <span data-ttu-id="30d8a-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30d8a-126">RELATED LINKS</span></span>

[<span data-ttu-id="30d8a-127">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="30d8a-127">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="30d8a-128">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="30d8a-128">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="30d8a-129">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="30d8a-129">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

