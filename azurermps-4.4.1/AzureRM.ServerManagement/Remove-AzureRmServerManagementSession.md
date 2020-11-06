---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 7476E6DC-6DE6-4199-A680-5717053A8CC5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
ms.openlocfilehash: d34678b6ff7996eabf807c92a84d647af15f6a71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516019"
---
# <span data-ttu-id="fc012-101">Remove-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="fc012-101">Remove-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="fc012-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fc012-102">SYNOPSIS</span></span>
<span data-ttu-id="fc012-103">Rimuove una sessione di gestione del server.</span><span class="sxs-lookup"><span data-stu-id="fc012-103">Removes a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc012-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc012-104">SYNTAX</span></span>

### <span data-ttu-id="fc012-105">ByName</span><span class="sxs-lookup"><span data-stu-id="fc012-105">ByName</span></span>
```
Remove-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc012-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="fc012-106">ByObject</span></span>
```
Remove-AzureRmServerManagementSession [[-SessionName] <String>] [-Session] <Session>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc012-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc012-107">DESCRIPTION</span></span>
<span data-ttu-id="fc012-108">Il cmdlet **Remove-AzureRmServerManagementSession** rimuove una sessione di gestione di Azure server.</span><span class="sxs-lookup"><span data-stu-id="fc012-108">The **Remove-AzureRmServerManagementSession** cmdlet removes an Azure Server Management session.</span></span>

## <span data-ttu-id="fc012-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc012-109">EXAMPLES</span></span>

## <span data-ttu-id="fc012-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fc012-110">PARAMETERS</span></span>

### <span data-ttu-id="fc012-111">-NodeName</span><span class="sxs-lookup"><span data-stu-id="fc012-111">-NodeName</span></span>
<span data-ttu-id="fc012-112">Specifica il nome del nodo in cui questo cmdlet rimuove la sessione.</span><span class="sxs-lookup"><span data-stu-id="fc012-112">Specifies the name of the node on which this cmdlet removes the session.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc012-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc012-113">-ResourceGroupName</span></span>
<span data-ttu-id="fc012-114">Specifica il nome del gruppo di risorse a cui appartiene la sessione.</span><span class="sxs-lookup"><span data-stu-id="fc012-114">Specifies the name of the resource group that the session belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc012-115">-Sessione</span><span class="sxs-lookup"><span data-stu-id="fc012-115">-Session</span></span>
<span data-ttu-id="fc012-116">Specifica la sessione rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc012-116">Specifies the session that this cmdlet removes.</span></span>

<span data-ttu-id="fc012-117">Questo parametro può essere usato al posto dei parametri *ResourceGroupName* , *NodeName* e *sessionname* .</span><span class="sxs-lookup"><span data-stu-id="fc012-117">This parameter may be used instead of the *ResourceGroupName* , *NodeName* and *SessionName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Session
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc012-118">-Sessionname</span><span class="sxs-lookup"><span data-stu-id="fc012-118">-SessionName</span></span>
<span data-ttu-id="fc012-119">Specifica il nome della sessione rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc012-119">Specifies the name of the session that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByObject
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc012-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc012-120">-DefaultProfile</span></span>
<span data-ttu-id="fc012-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fc012-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc012-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc012-122">CommonParameters</span></span>
<span data-ttu-id="fc012-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc012-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc012-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc012-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc012-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fc012-125">INPUTS</span></span>

### <span data-ttu-id="fc012-126">Sessione</span><span class="sxs-lookup"><span data-stu-id="fc012-126">Session</span></span>
<span data-ttu-id="fc012-127">Il parametro "Session" accetta il valore di tipo "Session" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="fc012-127">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="fc012-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc012-128">OUTPUTS</span></span>

## <span data-ttu-id="fc012-129">Note</span><span class="sxs-lookup"><span data-stu-id="fc012-129">NOTES</span></span>

## <span data-ttu-id="fc012-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc012-130">RELATED LINKS</span></span>

[<span data-ttu-id="fc012-131">Get-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="fc012-131">Get-AzureRmServerManagementSession</span></span>](./Get-AzureRmServerManagementSession.md)

[<span data-ttu-id="fc012-132">New-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="fc012-132">New-AzureRmServerManagementSession</span></span>](./New-AzureRmServerManagementSession.md)


