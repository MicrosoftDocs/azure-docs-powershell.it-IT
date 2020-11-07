---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 686785F8-2085-4705-A74D-12B18A87E187
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 4b63568b4a2bfd6b79c51fcd906819f4831a7ade
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687069"
---
# <span data-ttu-id="20ee1-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="20ee1-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="20ee1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="20ee1-102">SYNOPSIS</span></span>
<span data-ttu-id="20ee1-103">Ottiene un Vault di conservazione a lungo termine del server.</span><span class="sxs-lookup"><span data-stu-id="20ee1-103">Gets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20ee1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20ee1-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerBackupLongTermRetentionVault [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20ee1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20ee1-105">DESCRIPTION</span></span>
<span data-ttu-id="20ee1-106">Il cmdlet **Get-AzureRmSqlServerBackupLongTermRetentionVault** ottiene il Vault di conservazione a lungo termine registrato nel server.</span><span class="sxs-lookup"><span data-stu-id="20ee1-106">The **Get-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet gets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="20ee1-107">Il Vault è una risorsa di backup di Azure usata per archiviare i dati di backup.</span><span class="sxs-lookup"><span data-stu-id="20ee1-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="20ee1-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20ee1-108">EXAMPLES</span></span>

## <span data-ttu-id="20ee1-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="20ee1-109">PARAMETERS</span></span>

### <span data-ttu-id="20ee1-110">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20ee1-110">-ResourceGroupName</span></span>
<span data-ttu-id="20ee1-111">Specifica il nome del gruppo di risorse che contiene il server.</span><span class="sxs-lookup"><span data-stu-id="20ee1-111">Specifies the name of the resource group that contains the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20ee1-112">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="20ee1-112">-ServerName</span></span>
<span data-ttu-id="20ee1-113">Specifica il server per cui questo cmdlet ottiene un Vault.</span><span class="sxs-lookup"><span data-stu-id="20ee1-113">Specifies the server for which this cmdlet gets a vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20ee1-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="20ee1-114">-Confirm</span></span>
<span data-ttu-id="20ee1-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20ee1-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ee1-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20ee1-116">-WhatIf</span></span>
<span data-ttu-id="20ee1-117">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="20ee1-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20ee1-118">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="20ee1-118">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ee1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20ee1-119">-DefaultProfile</span></span>
<span data-ttu-id="20ee1-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="20ee1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20ee1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20ee1-121">CommonParameters</span></span>
<span data-ttu-id="20ee1-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20ee1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20ee1-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20ee1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20ee1-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="20ee1-124">INPUTS</span></span>

## <span data-ttu-id="20ee1-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20ee1-125">OUTPUTS</span></span>

## <span data-ttu-id="20ee1-126">Note</span><span class="sxs-lookup"><span data-stu-id="20ee1-126">NOTES</span></span>

## <span data-ttu-id="20ee1-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20ee1-127">RELATED LINKS</span></span>

[<span data-ttu-id="20ee1-128">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="20ee1-128">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Set-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="20ee1-129">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="20ee1-129">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

